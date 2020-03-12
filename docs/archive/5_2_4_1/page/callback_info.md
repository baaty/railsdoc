---
layout: archive_page
---
### コールバックとは
コールバックとは、オブジェクトが変わる時に実行できる処理のこと  
コールバックを使うことによって、モデルの作成後や保存前などに実行できるコードを書くことが可能

### コールバックの種類
#### メソッド参照例
    before_destroy :delete_parents
    private
      def delete_parents
        self.class.delete_by(parent_id: id)
      end

#### コールバックオブジェクト
    class BankAccount < ActiveRecord::Base
      before_save      EncryptionWrapper.new
      after_save       EncryptionWrapper.new
      after_initialize EncryptionWrapper.new
    end
    class EncryptionWrapper
      def before_save(record)
        record.credit_card_number = encrypt(record.credit_card_number)
      end
      def after_save(record)
        record.credit_card_number = decrypt(record.credit_card_number)
      end
      alias_method :after_initialize, :after_save
      private
        def encrypt(value)
          # Secrecy is committed
        end
        def decrypt(value)
          # Secrecy is unveiled
        end
    end