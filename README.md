# Bcash example for friend

An simple example


## How to use ?

Create database, migration and populate database

```ruby
$ rake db:create && rake db:migrate && rake db:seeds
```

### You need see
``` ruby
app/controllers/items_controller.rb
```

check action in controller called payment
``` ruby
items = []
items << Bcash::Item.new(id: @item.id, description: @item.name, amount: 1, price: @item.price)
package = Bcash::Package.create(items, 0 ,Bcash::PAD, url_retorno: 'http://meu-site.com.br') # O zero representa o valor do frete,altere o valor de acordo com sua necessidade
@payment = Bcash::Payment.new(package, email_loja: 'leiarf@gmail.com')
```


check VIEW in app/views/items/payment.html.erb


Bye bye, good luck! =)