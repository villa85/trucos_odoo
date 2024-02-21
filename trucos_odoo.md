# 16.0

1- Como mostrar informacion en un campo en dependencia de la seleccion de otro campo 
Ejemplo:
Necesito que el campo llamado amount_total muestre el total de lo que ya trae el  presupuesto sale.order, es decir que cuando yo elija el presupuesto se me autocomplete en otro campo el amount_total
    
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
```
# 17.0   Error "Since 17.0, the "attrs" and "states" attributes are no longer used."
Esto se debe a que en la version 17 desaparece las etiquetas "attrs" and "states". Aqui van algunos ejemplos de como arreglarlo

            attrs="{'invisible': [('imported','=',True)]}"/> (version 16)
            readonly = "imported == True"/> (version 17)

            attrs="{'readonly':[('state','!=','draft')],(version 16)
                    'invisible': [('move_type', 'not in', ('out_invoice', 'out_refund'))],(version 16)
                    'required': [('move_type', 'in', ('out_invoice', 'out_refund'))]}"(version 16)
            readonly = "state != 'draft'" (version 17)
            invisible = "move_type not in ['out_invoice','out_refund']"(version 17)
            required = "move_type in ['out_invoice','out_refund']"(version 17)
            
            attrs="{'invisible': ['|', '|',('payment_order_ok', '=', False),('state', '!=', 'posted'), ('move_type', 'not in', ('out_invoice', 'out_refund'))]}" (version 16)
            invisible = "payment_order_ok == False or state != 'posted' or move_type not in ['out_invoice','out_refund']"(version 17)

            attrs="{'invisible':['|',('lock', '=', True),('state','!=','Ongoing')]}" (version 16)
            invisible = "lock == False or state != 'Ongoing'"/> (version 17)

            attrs="{'readonly': [('imported','=',True)]}"/> (version 16)
            readonly = "imported == True"/> (version 17)

            attrs="{'required': [('count', '=', 0)]}" (version 16)
            modifiers="{'required': [('count', '=', 0)]}" (version 17)

            states="New" string="Confirm" type="object" (version 16)
            invisible="state != 'New'" string="Confirm" type="object" (version 17)

            states="Ongoing,Expire Soon," (version 16)
            invisible="state not in ['Ongoing','Expire Soon']" (version 17)

            states="draft" (version 16)
            invisible = "state != 'draft'" (version 17)

            states="draft,open,generated" (version 16)
            invisible = "state != 'draft' and state != 'open' and state != 'generated'" (version 17)


```
```
# 17.0 DeprecationWarning: Since 17.0: odoo.osv.osv.osv is deprecated, use odoo.models.Model

    Se arregla cambiando:
    from openerp.osv import osv (version 16)
    class res_partner(osv.osv): (version 16)
    
    from odoo import models (version 17)
    class res_partner(models.Model) (version 17)


# 17.0
```
    @api.multi (version 16) se arregla con  @api.model_create_multi (version 17)

```
```
```
# 17.0 Definición de un menu
```
        <record id="action_ftp_config_form" model="ir.actions.act_window" >
            <field name="name">FTP</field>
            <field name="res_model">ftp.config</field>
            <field name="view_mode">tree,form</field>
            <field name="limit">80</field>
        </record>

    <menuitem name="Configuración FTP" id="ftp_config_menu"  parent="base.menu_administration" sequence="20"/>

    <menuitem id="ftp_config_view"  name="Conexion FTP"  action="action_ftp_config_form" parent="ftp_config_menu" sequence="2"/>

            
```
# Clase SSH en Windows
```

