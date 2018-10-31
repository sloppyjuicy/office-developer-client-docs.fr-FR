---
title: 'Chapitre 4 : Modification des données'
TOCTitle: 'Chapter 4: Editing Data'
ms:assetid: 822b7365-0926-6411-6fb4-30de032570f8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249563(v=office.15)
ms:contentKeyID: 48545974
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d859f7bc3a74dfde1841be87f4a8237af9b7c48a
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862253"
---
# <a name="chapter-4-editing-data"></a>Chapitre 4 : Modification des données


**S’applique à**: Access 2013 | Office 2013

Les deux chapitres précédents ont expliqué comment utiliser ADO pour se connecter à une source de données, exécuter une commande, afficher les résultats dans un objet **Recordset** et naviguer dans le **jeu d'enregistrements**. Ce chapitre traite de la prochaine opération ADO fondamentale : la modification des données.

Ce chapitre continue d'utiliser l'exemple du **jeu d'enregistrements** présenté dans le chapitre 3  avec un changement important. Le code suivant est utilisé pour ouvrir le **jeu d'enregistrements**:

```vb 
 
 . . . 
'BeginEditIntro 
 Dim strSQL As String 
 Dim objRs1 As ADODB.Recordset 
 
 strSQL = "SELECT * FROM Shippers" 
 
 Set objRs1 = New ADODB.Recordset 
 
 objRs1.Open strSQL, GetNewConnection, adOpenStatic, _ 
 adLockBatchOptimistic, adCmdText 
 
 ' Disconnect the Recordset from the Connection object. 
 Set objRs1.ActiveConnection = Nothing 
'EndEditIntro 
 
 
 . . . 
```

Le changement important du code implique de définir la propriété **CursorLocation** de l'objet **Connection** sur **adUseClient** dans la fonction GetNewConnection (mentionnée ci-après), ce qui indique l'utilisation d'un curseur client. Pour en savoir plus sur les différences entre les curseurs côté client et côté serveur, reportez-vous au [Chapitre 8 : Présentation des curseurs et des verrous](chapter-8-understanding-cursors-and-locks.md).

Le paramètre **adUseClient** de la propriété **CursorLocation** déplace l'emplacement du curseur de la source de données (dans ce cas, le serveur SQL) vers l'emplacement du code client (la station de travail). Ce paramètre force ADO à invoquer le moteur de curseur client pour OLE DB du client pour créer et gérer le curseur.

Vous avez probablement aussi remarqué que le paramètre **LockType** de la méthode **Open** a désormais la valeur **adLockBatchOptimistic**. Ceci permet d'ouvrir le curseur en mode par lots. (Le fournisseur met plusieurs changements en cache et les écrit dans la source de données sous-jacente uniquement lorsque vous utilisez la méthode **UpdateBatch**.) Les modifications apportées au **jeu d'enregistrements** ne sont pas prises en compte dans la base de données tant que la méthode **UpdateBatch** n'est pas invoquée.

Enfin, le code de ce chapitre utilise une version modifiée de la fonction GetNewConnection, présentée au chapitre 2. Cette version de la fonction renvoie désormais un curseur côté client. La fonction est représentée comme suit :

```vb 
 
'BeginNewConnection 
Public Function GetNewConnection() As ADODB.Connection 
 Dim objConn1 As ADODB.Connection 
 Set objConn1 = New ADODB.Connection 
 
 strConnStr = "Provider=SQLOLEDB;Initial Catalog=Northwind;" & _ 
 "Data Source=MySrvr;Integrated Security=SSPI;" 
 
 objConn1.ConnectionString = strConnStr 
 objConn1.CursorLocation = adUseClient 
 objConn1.Open 
 
 Set GetNewConnection = objConn1 
End Function 
'EndNewConnection 
```

Ce chapitre présente les rubriques suivantes :

- [Modification d’enregistrements existants](editing-existing-records.md)

- [Identification des éléments pris en charge](determining-what-is-supported.md)

- [Suppression d’enregistrements à l’aide de la méthode Delete](deleting-records-using-the-delete-method.md)

- [Alternatives : Utilisation d’instructions SQL](alternatives-using-sql-statements.md)

- [Adding Records (ADO)](adding-records.md)