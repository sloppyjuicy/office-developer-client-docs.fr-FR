---
title: Propriété Database.ReplicaID (DAO)
TOCTitle: ReplicaID Property
ms:assetid: cf2ca8a1-d13f-30e0-2ca1-dd32ac736c56
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834672(v=office.15)
ms:contentKeyID: 48547805
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053375
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2ada9bf23a4b8fc34c5f9b4f24350fc6af91dc85
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703929"
---
# <a name="databasereplicaid-property-dao"></a>Propriété Database.ReplicaID (DAO)


**S’applique à**: Access 2013, Office 2013


Renvoie une valeur de 16 octets qui identifie de façon unique un réplica de base de données (espaces de travail Microsoft Access uniquement).

## <a name="syntax"></a>Syntaxe

*expression* . ReplicaID

*expression* Variable qui représente un objet de **base de données** .

## <a name="remarks"></a>Remarques

La valeur de retour est une valeur **GUID** qui identifie de façon unique le réplica ou le réplica-maître.

Le moteur de base de données Microsoft Access génère automatiquement cette valeur lorsque vous créez un nouveau réplica.

La propriété **ReplicaID** de chaque réplica (et réplica-maître) est stockée dans la table système MSysReplicas.

## <a name="example"></a>Exemple

Cet exemple réalise un réplica à partir du réplica-maître de Northwind.mdb puis renvoie la valeur de la propriété **ReplicaID** du réplica, automatiquement créée par le moteur de base de données Microsoft Access. (Si vous n'avez pas encore créé de réplica-maître de Northwind, consultez la propriété **Replicable** ou remplacez le nom de la base de données figurant dans le code par un réplica-maître existant.)

```vb 
Sub MakeReplicaReplicaIDX() 
 
 Dim dbsNorthwind As Database 
 Dim prpReplicaID As Property 
 Dim dbsReplica As Database 
 
 Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
 
 ' Makes a new replica. 
 dbsNorthwind.MakeReplica "Nwreplica2.mdb", _ 
 "second replica" 
 dbsNorthwind.Close 
 
 ' Opens the new replica to read its ReplicaID. 
 Set dbsReplica = OpenDatabase("Nwreplica2.mdb") 
 
 Debug.Print dbsReplica.ReplicaID 
 dbsReplica.Close 
 
End Sub 
 
```

