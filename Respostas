select * from customers c
where not exists (select o.order_id from orders o where o.customer_id = c.customer_id);

select * from products p
where not exists (select o.item_id from order_items o where o.product_id = p.product_id);

select * from products p
inner join stocks s on
s.product_id = p.product_id
where s.quantity = 0;

select s.store_name, count(*) as qtd_vendas from orders o
inner join stores s on
s.store_id = o.store_id
group by s.store_name;

select b.brand_name, s.store_name, count(*) as quantidade_vendas from brands b
inner join products p on
p.brand_id = b.brand_id
inner join order_items o on
o.product_id = p.product_id
inner join orders on ord
ord.order_id = o.order_id
inner join stores on s
s.store_id = ord.store_id
group by b.brand_name, s.store_name;

select * from staffs s
where not exists (select o.order_id from orders o where o.staff_id = s.staff_id);
