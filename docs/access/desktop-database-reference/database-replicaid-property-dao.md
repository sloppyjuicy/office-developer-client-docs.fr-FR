---
title: Database.ReplicaID Property (DAO)
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
ms.openlocfilehash: ca879a3c56d23a67987d86b7fbc21421cd8db843
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469113"
---
# <a name="databasereplicaid-property-dao"></a><span data-ttu-id="327e9-102">Database.ReplicaID Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="327e9-102">Database.ReplicaID Property (DAO)</span></span>


<span data-ttu-id="327e9-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="327e9-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="327e9-104">Renvoie une valeur de 16 octets qui identifie de façon unique un réplica de base de données (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="327e9-104">Returns a 16-byte value that uniquely identifies a database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="327e9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="327e9-105">Syntax</span></span>

<span data-ttu-id="327e9-106">*expression* . ReplicaID</span><span class="sxs-lookup"><span data-stu-id="327e9-106">*expression* .ReplicaID</span></span>

<span data-ttu-id="327e9-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="327e9-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="327e9-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="327e9-108">Remarks</span></span>

<span data-ttu-id="327e9-109">La valeur de retour est une valeur **GUID** qui identifie de façon unique le réplica ou le réplica-maître.</span><span class="sxs-lookup"><span data-stu-id="327e9-109">The return value is a **GUID** value that uniquely identifies the replica or Design Master.</span></span>

<span data-ttu-id="327e9-110">Le moteur de base de données Microsoft Access génère automatiquement cette valeur lorsque vous créez un nouveau réplica.</span><span class="sxs-lookup"><span data-stu-id="327e9-110">The Microsoft Access database engine automatically generates this value when you create a new replica.</span></span>

<span data-ttu-id="327e9-111">La propriété **ReplicaID** de chaque réplica (et réplica-maître) est stockée dans la table système MSysReplicas.</span><span class="sxs-lookup"><span data-stu-id="327e9-111">The **ReplicaID** property of each replica (and the Design Master) is stored in the MSysReplicas system table.</span></span>

## <a name="example"></a><span data-ttu-id="327e9-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="327e9-112">Example</span></span>

<span data-ttu-id="327e9-p101">Cet exemple réalise un réplica à partir du réplica-maître de Northwind.mdb puis renvoie la valeur de la propriété **ReplicaID** du réplica, automatiquement créée par le moteur de base de données Microsoft Access. (Si vous n'avez pas encore créé de réplica-maître de Northwind, consultez la propriété **Replicable** ou remplacez le nom de la base de données figurant dans le code par un réplica-maître existant.)</span><span class="sxs-lookup"><span data-stu-id="327e9-p101">This example makes a replica from the Design Master of Northwind.mdb, and then returns the replica's **ReplicaID**, which is automatically created by the Microsoft Access database engine. (If you have not yet created a Design Master of Northwind, refer to the **Replicable** property, or change the name of the database in the code to an existing Design Master.)</span></span>

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

