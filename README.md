select distinct customers.last_name,customers.phone,company_products.name,suppliers.contact_name
from customers join company_orders
on customers.id = company_orders.customer_id
join order_items on company_orders.id = order_items.order_id
join company_products on company_products.id = order_items.product_id
join suppliers on company_products.supplier_id = suppliers.id;

EDITOR = http://ec2-3-108-196-161.ap-south-1.compute.amazonaws.com/editor
