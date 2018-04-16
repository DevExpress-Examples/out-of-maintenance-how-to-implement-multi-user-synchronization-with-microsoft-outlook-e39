# How to implement multi-user synchronization with Microsoft Outlook


<p>Problem:</p><p>I'm planning to implement a multi-user scheduling smart client application, which should be capable of synchronizing the data with Microsoft Outlook. Each user has a unique name (UserId).<br />
How can I manage only specific appointments using the current user login information and perform an Outlook synchronization per user?</p><p>Solution:</p><p>To identify an appointment with a particular end-user, define a custom field mapping for the UserID. Then, populate the DataSet instance using the UserID as the query parameter of the TableAdapter. Update the SchedulerStorage.DataSource property with the DataSet instance.<br />
When synchronizing appointments with Microsoft Outlook, a UserProperty is used to save the UserID value along with Outlook appointment, so that it can be identified when performing the synchronization. The UserProperty represents a custom property of an Outlook Appointment item.</p>

<br/>


