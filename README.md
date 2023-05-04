Download Link: https://assignmentchef.com/product/solved-csci-3287-project-2-introduction-to-the-cassandra-key-value-store
<br>
<strong> </strong><strong>Description</strong>

In this project you will work with the Apache Cassandra database.  Cassandra is a key-value store database, essentially a giant hash table.

<strong>Procedure</strong>

To complete this project you will need to install Cassandra and the C++ bindings for the database.  All documentation regarding the Apache Cassandra project can be found at <strong>http://cassandra.apache.org/</strong>

Cassandra is designed in a way that is quite similar to MySQL.  A server daemon runs on your system continuously and you use clients running in various languages that connect via network connections to the daemon.  You will write a simple client program that allows you to exercise the Cassandra database from a simple command line written in C





Your program should maintain a current keyspace.  You can print this keyspace name along with your prompt.




Your program should accept five commands:




<ul>

 <li>Show all the available keyspaces</li>

</ul>




<strong>cassandra&gt; show</strong>




<ul>

 <li>List the contents of the current keyspace</li>

</ul>




<strong>cassandra&gt; list</strong>




<ul>

 <li>Set the current keyspace and table. You do NOT need to create a new keyspace and/or a new table if it does not already exist.</li>

</ul>




<strong>cassandra&gt; use </strong><em>&lt;keyspace&gt;</em><strong><em>.</em></strong><em>&lt;table&gt;</em>




<ul>

 <li>Retrieve the data associated with a key</li>

</ul>




<strong>cassandra&gt; get </strong><em>&lt;key&gt;</em>




<ul>

 <li>Insert a value in the database associated with a key</li>

</ul>




<strong>cassandra&gt; insert </strong><em>&lt;key&gt;</em>  <em>&lt;value&gt;</em>




where <em>&lt;key&gt;</em> and <em>&lt;value&gt;</em> should be any value legally allowed by Cassandra for insertion and retrieval.




A skeleton of the command line interface program will be provided.




<strong>Testing</strong>




Use cqlsh to create a keyspace and a table.  When you create the table, give it a single attribute (of any type) as its primary key.  Now in your client, you should be able to “use” the keyspace and table you created using cqlsh.  You can then perform your inserts and gets using the name of the single primary key attribute.  We’ll only test for one value being inserted and then retrieved.  The value can be of any type.