---
title: Database.DesignMasterID, propriété (DAO)
TOCTitle: DesignMasterID Property
ms:assetid: c0545561-d44f-5479-8ae0-e3955db91761
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822824(v=office.15)
ms:contentKeyID: 48547508
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a189d16880fccdc34c169aee61c6781e1d86afa8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294931"
---
# <a name="databasedesignmasterid-property-dao"></a><span data-ttu-id="4961a-102">Database.DesignMasterID, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="4961a-102">Database.DesignMasterID property (DAO)</span></span>

<span data-ttu-id="4961a-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4961a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4961a-104">Définit ou renvoie une valeur de 16 octets qui identifie de façon unique le réplica-maître d’un jeu de réplicas (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="4961a-104">Sets or returns a 16-byte value that uniquely identifies the Design Master in a replica set (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4961a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4961a-105">Syntax</span></span>

<span data-ttu-id="4961a-106">*.* DesignMasterID</span><span class="sxs-lookup"><span data-stu-id="4961a-106">*expression* .DesignMasterID</span></span>

<span data-ttu-id="4961a-107">*expression* Variable qui représente un objet **Database**.</span><span class="sxs-lookup"><span data-stu-id="4961a-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4961a-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="4961a-108">Remarks</span></span>

<span data-ttu-id="4961a-p101">Vous ne devez définir la propriété **DesignMasterID** que si vous souhaitez déplacer le réplica-maître actif. Si vous définissez cette propriété, un réplica spécifique du jeu de réplicas devient le réplica-maître.</span><span class="sxs-lookup"><span data-stu-id="4961a-p101">You should set the **DesignMasterID** property only if you need to move the current Design Master. Setting this property makes a specific replica in the replica set the Design Master.</span></span>

> [!NOTE]
> <span data-ttu-id="4961a-p102">[!REMARQUE] Ne créez jamais de deuxième réplica-maître dans un jeu de réplicas, car sa présence peut entraîner la perte de données.</span><span class="sxs-lookup"><span data-stu-id="4961a-p102">Never create a second Design Master in a replica set. The existence of a second Design Master can result in the loss of data.</span></span>

<span data-ttu-id="4961a-p103">Dans des cas extrêmes (effacement ou endommagement du réplica-maître, par exemple), vous pouvez définir cette propriété sur le réplica actif. Toutefois, si vous la définissez sur un réplica alors que le jeu contient déjà un autre réplica-maître, vous risquez de fractionner le jeu de réplicas en deux jeux incompatibles et d'empêcher toute synchronisation ultérieure des données.</span><span class="sxs-lookup"><span data-stu-id="4961a-p103">Under extreme circumstances— for example, if the Design Master is erased or corrupted— you can set this property at the current replica. However, setting this property at a replica when there is already another Design Master in the set might partition your replica set into two irreconcilable sets and prevent any further synchronization of data.</span></span>

<span data-ttu-id="4961a-p104">Si vous définissez un réplica comme nouveau réplica-maître du jeu, synchronisez-le avec tous les réplicas du jeu de réplicas avant de définir la propriété **DesignMasterID** du réplica. Dans ce cadre, le réplica doit être ouvert en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="4961a-p104">If you decide to make a replica the new Design Master for the set, synchronize it with all the replicas in the replica set before setting the **DesignMasterID** property in the replica. The replica must be open in exclusive mode in order to make it the Design Master.</span></span>

<span data-ttu-id="4961a-117">Si vous définissez un réplica en lecture seule comme réplica-maître, le réplica cible est en lecture/écriture. L'ancien réplica-maître reste également en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="4961a-117">If you make a replica that is designated read-only into the Design Master, the target replica is made read/write; the old Design Master also remains read/write.</span></span>

<span data-ttu-id="4961a-118">Le paramètre de la propriété **DesignMasterID** est enregistré dans la table système MSysRepInfo.</span><span class="sxs-lookup"><span data-stu-id="4961a-118">The **DesignMasterID** property setting is stored in the MSysRepInfo system table.</span></span>

## <a name="example"></a><span data-ttu-id="4961a-119">Exemple</span><span class="sxs-lookup"><span data-stu-id="4961a-119">Example</span></span>

<span data-ttu-id="4961a-p105">L'exemple ci-dessous définit la propriété **DesignMasterID** sur le paramètre de propriété **ReplicaID** d'une autre base de données, qui devient alors le réplica-maître du jeu de réplicas. L'ancien réplica-maître et le nouveau sont synchronisés afin de répercuter la modification de la structure. Pour que ce code puisse fonctionner, vous devez créer un réplica-maître et un réplica, inclure leur nom et leur chemin d'accès, puis exécuter ce code à partir d'une autre base de données que l'ancien réplica-maître ou le nouveau.</span><span class="sxs-lookup"><span data-stu-id="4961a-p105">This example sets the **DesignMasterID** property to the **ReplicaID** property setting of another database, making that database the Design Master in the replica set. The old and new Design Masters are synchronized to update the design change. For this code to work, you must create a Design Master and replica, include their names and paths as appropriate, and run this code from a database other than the old or new Design Master.</span></span>

```vb 
 Sub SetNewDesignMaster(strOldDM as String, _ 
    strNewDM as String) 
    
    Dim dbsOld As Database 
    Dim dbsNew As Database 
    
    ' Open the current Design Master in exclusive mode. 
    Set dbsOld = OpenDatabase(strOldDM, True) 
    
    ' Open the database that will become the new 
    ' Design Master. 
    Set dbsNew = OpenDatabase(strNewDM) 
    
    ' Make the new database the Design Master. 
    dbsOld.DesignMasterID = dbsNew.ReplicaID 
    
    ' Synchronize the old Design Master with the new 
    ' Design Master, and allow two-way exchanges. 
    dbsOld.Synchronize strNewDM, dbRepImpExpChanges 
    dbsOld.Close 
    dbsNew.Close 
 
 End Sub 
 
```

