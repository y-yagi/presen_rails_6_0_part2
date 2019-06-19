#### [Add a configuration option to customize format of the `ActiveModel::Errors#full_message`](https://github.com/rails/rails/pull/32956)

```
activemodel.errors.models.person/contacts/addresses.attributes.street.format
activemodel.errors.models.person/contacts/addresses.format
activemodel.errors.models.person.attributes.name.format
activemodel.errors.models.person.format
```

* のように、model + attributes + format、又は、model + formatのkeyを追加で見るようになっている
* なお、上記は、config.active_model.i18n_customize_full_messageをtrueにした場合のみ有効(デフォルトはfalse)
