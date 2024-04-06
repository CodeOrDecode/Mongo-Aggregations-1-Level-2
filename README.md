1. db.orders.aggregate([{$match:{customer_id:1}}])

2. db.products.aggregate([{$match:{supplier_id:3}}])

3. db.orders.aggregate([{$match:{status:"shipped"}}])

4. db.payments.aggregate([{$match:{paymentMethod:{$ne:"UPI"}}} ,{$project:{amount:1,paymentMethod:1}}])

5.  db.payments.aggregate([{$match:{amount:{$gt:100}}} ,{$project:{paymentstatus:1}}])

6.  db.orderdetails.aggregate([{$match:{price:{$gt:2000}}} ,{$project:{shipper_id:1,price:1}}])

7. db.orders.aggregate([{$match:{status:{$ne:"shipped"}}} ,{$project:{_id:1,customer_id:1}}])

8. db.products.aggregate([{$match:{category_id:{$eq:1}}} ,{$project:{_id:0}}])

9. db.products.aggregate([{$match:{price:{$gt:1500}}} ,{$project:{name:1,quantity:1}}])

10. db.shippers.aggregate([{$match:{phone:{$eq:"1-800-742-5877"}}} ,{$project:{name:1}}])

11. db.suppliers.aggregate([{$match:{name:{$eq:"Sony"}}} ,{$project:{city:1,phone:1}}])

12. db.suppliers.aggregate([{$match:{city:{$eq:"Tokyo"}}} ,{$project:{name:1}}])

13. db.payments.aggregate([{$match:{paymentMethod:{$eq:"UPI"}}} ,{$project:{amount:1}}])

14. db.buyers.aggregate([{$match:{email:{$eq:"john@hotmail.com"}}} ,{$project:{city:"$address.city"}}])

15. db.orders.aggregate([{$match:{status:{$eq:"shipped"}}},{$limit:5} ,{$project:{order_date:1,status:1,total:1}}])

16. 
