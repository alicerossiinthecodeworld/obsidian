**select**  sm.Name, p.PostingNumber, pb.ID, p.*, p.PostingStateID, pi2.*  **from** Posting p 

**left** **join** PostingInPostingBatch pipb **on** p.id = pipb.PostingID 

**left** **join** postingbatch pb **on** pb.ID = pipb.PostingBatchID 

**left** **join** sortmethod sm **on** sm.id = pb.sortmethodid

**join** PostingItem pi2 **on** p.ID = pi2.PostingID 

**where** postingnumber =

#запрос [[работа]]  [[озон]] #sql 