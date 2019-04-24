---
title: Méthode Database. MakeReplica (DAO)
TOCTitle: MakeReplica Method
ms:assetid: b6bf4982-0804-12ce-849f-d2b4ac2e48a5
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822413(v=office.15)
ms:contentKeyID: 48547286
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053371
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 9b9e2eac360d157f28b986b6598ade58b8c34ec6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294917"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="729cd-102">Méthode Database. MakeReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="729cd-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="729cd-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="729cd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="729cd-104">Crée un nouveau réplica à partir d’un autre réplica de base de données (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="729cd-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="729cd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="729cd-105">Syntax</span></span>

<span data-ttu-id="729cd-106">*expression* . MakeReplica (***pathname***, ***Description***, ***options***)</span><span class="sxs-lookup"><span data-stu-id="729cd-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="729cd-107">*expression* Variable qui représente un objet **Database** .</span><span class="sxs-lookup"><span data-stu-id="729cd-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="729cd-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="729cd-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="729cd-109">Nom</span><span class="sxs-lookup"><span data-stu-id="729cd-109">Name</span></span></p></th>
<th><p><span data-ttu-id="729cd-110">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="729cd-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="729cd-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="729cd-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="729cd-112">Description</span><span class="sxs-lookup"><span data-stu-id="729cd-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="729cd-113"><em>PathName</em></span><span class="sxs-lookup"><span data-stu-id="729cd-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="729cd-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="729cd-114">Required</span></span></p></td>
<td><p><span data-ttu-id="729cd-115"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="729cd-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="729cd-116">Chemin d'accès et nom de fichier du nouveau réplica.</span><span class="sxs-lookup"><span data-stu-id="729cd-116">The path and file name of the new replica.</span></span> <span data-ttu-id="729cd-117">Si l'argument réplica correspond à un nom de fichier existant, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="729cd-117">If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="729cd-118"><em>Description</em></span><span class="sxs-lookup"><span data-stu-id="729cd-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="729cd-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="729cd-119">Required</span></span></p></td>
<td><p><span data-ttu-id="729cd-120"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="729cd-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="729cd-121">Valeur de type <strong>String</strong> décrivant le réplica que vous créez.</span><span class="sxs-lookup"><span data-stu-id="729cd-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="729cd-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="729cd-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="729cd-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="729cd-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="729cd-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="729cd-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="729cd-125">Constante <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> qui spécifie les caractéristiques du réplica que vous créez.</span><span class="sxs-lookup"><span data-stu-id="729cd-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="729cd-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="729cd-126">Remarks</span></span>

<span data-ttu-id="729cd-127">Les propriétés **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** d'un réplica nouvellement créé sont toutes affectées de la valeur **False**, ce qui signifie que les tables ne comporteront pas de données.</span><span class="sxs-lookup"><span data-stu-id="729cd-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="729cd-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="729cd-128">Example</span></span>

<span data-ttu-id="729cd-129">Cette fonction s'appuie sur la méthode **MakeReplica** pour créer un réplica supplémentaire d'un réplica-maître existant.</span><span class="sxs-lookup"><span data-stu-id="729cd-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="729cd-130">L'argument Optionsint peut être une combinaison des constantes **dbRepMakeReadOnly** et **dbRepMakePartial**, ou il peut être égal à 0.</span><span class="sxs-lookup"><span data-stu-id="729cd-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="729cd-131">Par exemple, pour créer un réplica partiel en lecture seule, vous devez transmettre la valeur **dbRepMakeReadOnly** + **dbRepMakePartial** comme valeur de Optionsint.</span><span class="sxs-lookup"><span data-stu-id="729cd-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

```vb 
Function MakeAdditionalReplica(strReplicableDB As _ 
 String, strNewReplica As String, intOptions As _ 
 Integer) As Integer 
 
 Dim dbsTemp As Database 
 On Error GoTo ErrorHandler 
 
 Set dbsTemp = OpenDatabase(strReplicableDB) 
 
 ' If no options are passed to 
 ' MakeAdditionalReplica, omit the 
 ' options argument, which defaults to 
 ' a full, read/write replica. Otherwise, 
 ' use the value of intOptions. 
 
 If intOptions = 0 Then 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB 
 Else 
 dbsTemp.MakeReplica strNewReplica, _ 
 "Replica of " & strReplicableDB, _ 
 intOptions 
 End If 
 
 dbsTemp.Close 
 
ErrorHandler: 
 Select Case Err 
 Case 0: 
 MakeAdditionalReplica = 0 
 Exit Function 
 Case Else: 
 MsgBox "Error " & Err & " : " & Error 
 MakeAdditionalReplica = Err 
 Exit Function 
 End Select 
 
End Function 
 
```

