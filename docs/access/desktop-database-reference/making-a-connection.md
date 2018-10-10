---
title: Établissement d'une connexion
TOCTitle: Making a Connection
ms:assetid: 188f6794-f4ec-8e8d-5adc-bdee36f4c9ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248932(v=office.15)
ms:contentKeyID: 48543472
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f1deaeb3f636c95da2aec6a3cbf3a2d097455e36
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470108"
---
# <a name="making-a-connection"></a>Établissement d'une connexion

**S’applique à**: Access 2013 | Office 2013

Pour vous connecter à une source de données, vous devez spécifier une *chaîne de connexion*, dont les paramètres peuvent être différents en fonction des fournisseurs et des sources de données. Pour en savoir plus, reportez-vous à la rubrique [Création de la chaîne de connexion](creating-the-connection-string.md).

De manière générale, ADO ouvre une connexion à l'aide de la méthode **Connection** objet **Open**. La syntaxe de la méthode **Open** est illustrée ci-dessous :

```vb
Dim connection as New ADODB.Connection 
connection.Open ConnectionString, UserID, Password, OpenOptions
```

Vous pouvez également invoquer une technique de raccourci, **Recordset.Open**, pour ouvrir une connexion implicite et émettre une commande sur la connexion en une opération. Cela en passant une chaîne de connexion valide comme l’argument *ActiveConnection* de la méthode **Open** . La syntaxe pour chaque méthode dans Visual Basic est présentée ci-après :

```vb
Dim recordset as ADODB.Recordset 
Set recordset = New ADODB.Recordset 
recordset.Open Source, ActiveConnection, CursorType, LockType, Options
```

> [!NOTE]
> [!REMARQUE] Quand utiliser un objet **Connection** plutôt qu'un raccourci **Recordset.Open** ? Utilisez un objet **Connection** lorsque vous envisagez d'ouvrir plusieurs **jeux d'enregistrements** ou lorsque vous exécutez des commandes multiples. Une connexion est toujours implicitement créée par ADO lorsque vous utilisez le raccourci **Recordset.Open**.


