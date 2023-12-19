# 16.0

1- Como mostrar informacion en un campo en dependencia de la seleccion de otro campo 
Ejemplo:
Necesito que el campo llamado amount_total muestre el total de lo que ya trae el  presupuesto sale.order, es decir que cuando yo elija el presupuesto se me autocomplete en otro campo el amount_total
```
class RecurringContract(models.Model):
    _name = "recurring.contract"
    _inherit = ['mail.thread', 'mail.activity.mixin']

    budget_id = fields.Many2one('sale.order',string='Budget', help='To add budget reference')
    amount_total_budget = fields.Monetary(string='Amount Total',
    store=True,  # Almacenar el valor calculado en la base de datos
    compute='_compute_amount_total_budget',
    readonly=True # Hacer el campo de solo lectura,
    help='Show Total Amount')

        @api.depends('budget_id.amount_total')
    def _compute_amount_total_budget(self):
        for record in self:
            record.amount_total_budget = record.budget_id.amount_total if record.budget_id else 0.0
```

# 17.0
```
Error "Since 17.0, the "attrs" and "states" attributes are no longer used."
Esto se debe a que en la version 17 desaparece las etiquetas "attrs" and "states". Aqui van algunos ejemplos de como arreglarlo

            attrs="{'invisible': [('imported','=',True)]}"/> (version 16)
            readonly = "imported == True"/> (version 17)

            attrs="{'invisible':['|',('lock', '=', True),('state','!=','Ongoing')]}" (version 16)
            invisible = "lock == False or state != 'Ongoing'"/> (version 17)

            attrs="{'readonly': [('imported','=',True)]}"/> (version 16)
            readonly = "imported == True"/> (version 17)

            states="New" string="Confirm" type="object" (version 16)
            invisible="state != 'New'" string="Confirm" type="object" (version 17)

            states="Ongoing,Expire Soon," (version 16)
            invisible="state not in ['Ongoing','Expire Soon']" (version 17)


            
```

