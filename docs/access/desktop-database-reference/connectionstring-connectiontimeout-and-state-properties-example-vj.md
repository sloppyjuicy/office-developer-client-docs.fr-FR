---
title: ConnectionString, ConnectionTimeout et State, propriétés – Exemple (VJ++)
TOCTitle: ConnectionString, ConnectionTimeout, and State properties example (VJ++)
ms:assetid: 88b3f95e-0e46-7cbb-8086-d583319a6628
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249599(v=office.15)
ms:contentKeyID: 48546141
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 23f4e69229d0b3ac6a9fdbe1f60a68919826bfed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581685"
---
# <a name="connectionstring-connectiontimeout-and-state-properties-example-vj"></a>ConnectionString, ConnectionTimeout et State, propriétés – Exemple (VJ++)


**S’applique à** : Access 2013, Office 2013

Cet exemple illustre les différentes façons d'utiliser la propriété [ConnectionString](connectionstring-property-ado.md) pour ouvrir un objet [Connection](connection-object-ado.md). Elle utilise également la propriété [ConnectionTimeout](connectiontimeout-property-ado.md) pour définir un délai d'expiration de la connexion et la propriété [State](state-property-ado.md) pour vérifier l'état des connexions. La fonction GetState est nécessaire à l'exécution de cette procédure.

```java 
 
// BeginConnectionStringJ 
import com.ms.wfc.data.*; 
import java.io.* ; 
 
public class ConnectionStringX 
{ 
 // The main entry point for the application. 
 
 public static void main (String[] args) 
 { 
 ConnectionStringX(); 
 System.exit(0); 
 } 
 
 // ConnectionStringX function 
 
 static void ConnectionStringX() 
 { 
 // Define ADO Objects. 
 Connection cnConn1 = null; 
 Connection cnConn2 = null; 
 Connection cnConn3 = null; 
 Connection cnConn4 = null; 
 
 //Declarations. 
 
 BufferedReader in = 
 new BufferedReader (new InputStreamReader(System.in)); 
 String line = null; 
 String strTemp; 
 
 try 
 { 
 // Open a connection using OLE DB syntax. 
 cnConn1 = new Connection(); 
 cnConn1.setConnectionString( 
 "Provider='sqloledb';Data Source='MySqlServer';" + 
 "Initial Catalog='Pubs';Integrated Security='SSPI';"); 
 cnConn1.setCommandTimeout(30); 
 cnConn1.open(); 
 strTemp = getState(cnConn1.getState()); 
 System.out.println("CnConn1 state: " + strTemp); 
 
 // Open a connection using a DSN and ODBC tags. 
 // It is assumed that you have create DSN 'Pubs' with a user name as 
 // 'MyUserId' and password as 'MyPassword'. 
 cnConn2 = new Connection(); 
 cnConn2.setConnectionString("DSN='Pubs';UID='MyUserId';PWD='MyPassword';"); 
 cnConn2.open(); 
 strTemp = getState(cnConn2.getState()); 
 System.out.println("CnConn2 state: " + strTemp); 
 
 // Open a connection using a DSN and OLE DB tags. 
 cnConn3 = new Connection(); 
 cnConn3.setConnectionString 
 ("Data Source='Pubs';"); 
 cnConn3.open(); 
 strTemp = getState(cnConn3.getState()); 
 System.out.println("CnConn3 state: " + strTemp); 
 
 // Open a connection using a DSN and individual 
 // arguments instead of a connection string. 
 // It is assumed that you have create DSN 'Pubs' with a user name as 
 // 'MyUserId' and password as 'MyPassword'. 
 cnConn4 = new Connection(); 
 cnConn4.open("Pubs", "MyUserId", "MyPassword"); 
 strTemp = getState(cnConn4.getState()); 
 System.out.println("CnConn4 state: " + strTemp); 
 
 System.out.println("\n\nPress <Enter> to continue.."); 
 in.readLine(); 
 
 } 
 catch( AdoException ae ) 
 { 
 // Notify user of any errors that result from ADO. 
 
 System.out.println("Exception: " + ae.getMessage()); 
 
 } 
 
 // System read requires this catch. 
 catch( java.io.IOException je) 
 { 
 PrintIOError(je); 
 } 
 
 finally 
 { 
 // Cleanup objects before exit. 
 if (cnConn1 != null) 
 if (cnConn1.getState() == 1) 
 cnConn1.close(); 
 if (cnConn2 != null) 
 if (cnConn2.getState() == 1) 
 cnConn2.close(); 
 if (cnConn3 != null) 
 if (cnConn3.getState() == 1) 
 cnConn3.close(); 
 if (cnConn4 != null) 
 if (cnConn4.getState() == 1) 
 cnConn4.close(); 
 } 
 
 } 
 
 // getState Function 
 
 static String getState(int intState) 
 { 
 // Returns current state of the connection object. 
 String strState=null; 
 
 switch(intState) 
 { 
 case AdoEnums.ObjectState.CLOSED : 
 strState = new String("adStateClosed"); 
 break; 
 case AdoEnums.ObjectState.OPEN : 
 strState = new String("adStateOpen"); 
 break; 
 default : 
 break; 
 } 
 return strState; 
 } 
 
 // PrintIOError Function 
 
 static void PrintIOError( java.io.IOException je) 
 { 
 System.out.println("Error \n"); 
 System.out.println("\tSource = " + je.getClass() + "\n"); 
 System.out.println("\tDescription = " + je.getMessage() + "\n"); 
 } 
} 
 
// EndConnectionStringJ 
```

