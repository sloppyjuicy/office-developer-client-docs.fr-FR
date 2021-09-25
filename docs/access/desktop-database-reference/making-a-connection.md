---
title: Connexion
TOCTitle: Making a connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 5c63ad8329dddecfb8a5900a1ade860325629322
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581034"
---
# <a name="making-a-connection"></a>Connexion

**S’applique à** : Access 2013, Office 2013

Pour vous connecter à une source de données, vous devez spécifier une *chaîne de connexion*, dont les paramètres peuvent être différents en fonction des fournisseurs et des sources de données. Pour en savoir plus, reportez-vous à la rubrique [Création de la chaîne de connexion](creating-the-connection-string.md).

De manière générale, ADO ouvre une connexion à l'aide de la méthode **Connection** objet **Open**. La syntaxe de la méthode **Open** est illustrée ci-dessous :

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

Vous pouvez également invoquer une technique de raccourci, **Recordset.Open**, pour ouvrir une connexion implicite et émettre une commande sur la connexion en une opération. Pour ce faire, transférez une chaîne de connexion valide en tant qu'argument *ConnexionActive* à la méthode **Open**. La syntaxe pour chaque méthode dans Visual Basic est présentée ci-après :

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> [!REMARQUE] Quand utiliser un objet **Connection** plutôt qu'un raccourci **Recordset.Open** ? Utilisez un objet **Connection** lorsque vous envisagez d'ouvrir plusieurs **jeux d'enregistrements** ou lorsque vous exécutez des commandes multiples. Une connexion est toujours implicitement créée par ADO lorsque vous utilisez le raccourci **Recordset.Open**.


