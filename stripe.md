# stripe

### Link
[Stripe API Reference](https://stripe.com/docs/api)   
[Stripe.js API Reference](https://stripe.com/docs/js)

### Module
go get github.com/stripe/stripe-go/v72

### 認証
```
stripe.Key = "APIキー"
```

### アカウント新規作成
```
func NewAccount() {

    stripe.Key = "APIキー"

    params := &stripe.CustomerParams{
		Description: stripe.String("b8hpcg8hv3amvi9dol0g"),// 任意のstring
	}
	c, err := customer.New(params)
	}
```

### クレジットカードの追加
```
func AddCard()  {

    stripe.Key = "APIキー"

	params := &stripe.CardParams{
		Customer: stripe.String("顧客ID"),
		Token: stripe.String("tok_mastercard"),
	}
	c, err := card.New(params)

}
```