# extend Data Dump Queries

please use the following queries to generate a dump free of PII for us to replicate your environment. Please note that 2 files will be generated.
dump_data_structure_only.sql and dump_data_without_pii.sql. Simply create a zip file from these 2 sql files and send it to us.
 
## Command 1: dump_data_structure_only.sql

```mysqldump -u <your_user> -p <your_db> --no-data > dump_data_structure_only.sql```
 
## Command 2: dump_data_without_pii.sql

```
mysqldump -u <your_user> -p <your_db> --ignore-table=customer_address_entity --ignore-table=customer_address_entity_datetime --ignore-table=customer_address_entity_decimal --ignore-table=customer_address_entity_int --ignore-table=customer_address_entity_text --ignore-table=customer_address_entity_varchar --ignore-table=customer_entity --ignore-table=customer_entity_datetime --ignore-table=customer_entity_decimal --ignore-table=customer_entity_int --ignore-table=customer_entity_text --ignore-table=customer_entity_varchar --ignore-table=customer_grid_flat --ignore-table=customer_log --ignore-table=customer_visitor --ignore-table=newsletter_subscriber --ignore-table=product_alert_price --ignore-table=product_alert_stock --ignore-table=vault_payment_token --ignore-table=vault_payment_token_order_payment_link --ignore-table=wishlist --ignore-table=wishlist_item --ignore-table=wishlist_item_option --ignore-table=catalogsearch_recommendations --ignore-table=core_session --ignore-table=log_url --ignore-table=log_url_info --ignore-table=log_visitor --ignore-table=log_visitor_info \
--ignore-table=log_visitor_online --ignore-table=report_event --ignore-table=report_compared_product_index --ignore-table=report_viewed_product_aggregated_daily --ignore-table=report_viewed_product_aggregated_monthly --ignore-table=report_viewed_product_aggregated_yearly --ignore-table=report_viewed_product_index --ignore-table=quote --ignore-table=quote_address --ignore-table=quote_address_item --ignore-table=quote_id_mask --ignore-table=quote_item --ignore-table=quote_item_option --ignore-table=quote_payment --ignore-table=quote_shipping_rate --ignore-table=sales_order --ignore-table=sales_order_address --ignore-table=sales_order_aggregated_created --ignore-table=sales_order_aggregated_updated --ignore-table=sales_order_grid --ignore-table=sales_order_item --ignore-table=sales_order_payment --ignore-table=sales_order_status_history --ignore-table=sales_order_tax --ignore-table=sales_order_tax_item --ignore-table=sales_invoice --ignore-table=sales_invoice_comment --ignore-table=sales_invoiced_aggregated --ignore-table=sales_invoiced_aggregated_order --ignore-table=sales_invoice_grid \
--ignore-table=sales_invoice_item \
--ignore-table=sales_shipment --ignore-table=sales_shipment_comment --ignore-table=sales_shipment_grid --ignore-table=sales_shipment_item --ignore-table=sales_shipment_track --ignore-table=sales_shipping_aggregated --ignore-table=sales_shipping_aggregated_order --ignore-table=sales_creditmemo --ignore-table=sales_creditmemo_comment --ignore-table=sales_creditmemo_grid --ignore-table=sales_creditmemo_item --ignore-table=sales_refunded_aggregated --ignore-table=sales_refunded_aggregated_order --ignore-table=sales_payment_transaction --ignore-table=sales_bestsellers_aggregated_daily --ignore-table=sales_bestsellers_aggregated_monthly --ignore-table=sales_bestsellers_aggregated_yearly --ignore-table=paypal_billing_agreement --ignore-table=paypal_billing_agreement_order --ignore-table=paypal_payment_transaction --ignore-table=paypal_settlement_report --ignore-table=paypal_settlement_report_row > dump_data_without_pii.sql
 
```
 
