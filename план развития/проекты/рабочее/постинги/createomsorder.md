#постингкреатор #инфоосервисах #идеи #планы 

async createOmsOrder(delivery_type: OrderTypeDto,

wh_rezon_id: number,

item_id: number,

client_id?: number,

with_bag?: boolean,

postings_qty?: number,

item_qty?: number,

timeslot_id?: number) {

const { data } = await this.createOmsOrderCreateOmsOrderPost({

wh_rezon_id:wh_rezon_id, delivery_type:delivery_type, item_id:item_id, client_id:client_id, with_bag:with_bag, postings_qty:postings_qty, item_qty:item_qty, timeslot_id:timeslot_id

})

return data

}