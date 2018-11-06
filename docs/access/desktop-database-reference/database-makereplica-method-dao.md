---
title: Méthode Database.MakeReplica (DAO)
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
ms.openlocfilehash: 45aa005b7c8337a4c5541ea7217cbdb520bb1725
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997734"
---
# <a name="databasemakereplica-method-dao"></a><span data-ttu-id="c8884-102">Méthode Database.MakeReplica (DAO)</span><span class="sxs-lookup"><span data-stu-id="c8884-102">Database.MakeReplica method (DAO)</span></span>

<span data-ttu-id="c8884-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c8884-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c8884-104">Crée un nouveau réplica à partir d'un autre réplica de base de données (espaces de travail Microsoft Access uniquement).</span><span class="sxs-lookup"><span data-stu-id="c8884-104">Makes a new replica from another database replica (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c8884-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c8884-105">Syntax</span></span>

<span data-ttu-id="c8884-106">*expression* . MakeReplica (***chemin d’accès***, ***Description***, ***Options***)</span><span class="sxs-lookup"><span data-stu-id="c8884-106">*expression* .MakeReplica(***PathName***, ***Description***, ***Options***)</span></span>

<span data-ttu-id="c8884-107">*expression* Variable qui représente un objet de **base de données** .</span><span class="sxs-lookup"><span data-stu-id="c8884-107">*expression* A variable that represents a **Database** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c8884-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c8884-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c8884-109">Name</span><span class="sxs-lookup"><span data-stu-id="c8884-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c8884-110">Requis/facultatif</span><span class="sxs-lookup"><span data-stu-id="c8884-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c8884-111">Type de données</span><span class="sxs-lookup"><span data-stu-id="c8884-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c8884-112">Description</span><span class="sxs-lookup"><span data-stu-id="c8884-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c8884-113"><em>Chemin d’accès</em></span><span class="sxs-lookup"><span data-stu-id="c8884-113"><em>PathName</em></span></span></p></td>
<td><p><span data-ttu-id="c8884-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c8884-114">Required</span></span></p></td>
<td><p><span data-ttu-id="c8884-115"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="c8884-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c8884-p101">Chemin d'accès et nom de fichier du nouveau réplica. Si l'argument réplica correspond à un nom de fichier existant, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="c8884-p101">The path and file name of the new replica. If replica is an existing file name, then an error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c8884-118"><em>Description</em></span><span class="sxs-lookup"><span data-stu-id="c8884-118"><em>Description</em></span></span></p></td>
<td><p><span data-ttu-id="c8884-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c8884-119">Required</span></span></p></td>
<td><p><span data-ttu-id="c8884-120"><strong>Chaîne</strong></span><span class="sxs-lookup"><span data-stu-id="c8884-120"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="c8884-121">Valeur de type <strong>String</strong> décrivant le réplica que vous créez.</span><span class="sxs-lookup"><span data-stu-id="c8884-121">A <strong>String</strong> that describes the replica that you are creating</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c8884-122"><em>Options</em></span><span class="sxs-lookup"><span data-stu-id="c8884-122"><em>Options</em></span></span></p></td>
<td><p><span data-ttu-id="c8884-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c8884-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="c8884-124"><strong>Variante</strong></span><span class="sxs-lookup"><span data-stu-id="c8884-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c8884-125">Constante <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> qui spécifie les caractéristiques du réplica que vous créez.</span><span class="sxs-lookup"><span data-stu-id="c8884-125">A <strong><a href="replicatypeenum-enumeration-dao.md">ReplicaTypeEnum</a></strong> constant that specifies characteristics of the replica you are creating.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c8884-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="c8884-126">Remarks</span></span>

<span data-ttu-id="c8884-127">Les propriétés **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** d'un réplica nouvellement créé sont toutes affectées de la valeur **False**, ce qui signifie que les tables ne comporteront pas de données.</span><span class="sxs-lookup"><span data-stu-id="c8884-127">A newly created partial replica will have all **[ReplicaFilter](tabledef-replicafilter-property-dao.md)** properties set to **False**, meaning that no data will be in the tables.</span></span>

## <a name="example"></a><span data-ttu-id="c8884-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="c8884-128">Example</span></span>

<span data-ttu-id="c8884-129">Cette fonction s'appuie sur la méthode **MakeReplica** pour créer un réplica supplémentaire d'un réplica-maître existant.</span><span class="sxs-lookup"><span data-stu-id="c8884-129">This function uses the **MakeReplica** method to create an additional replica of an existing Design Master.</span></span> <span data-ttu-id="c8884-130">L’argument Optionsint peut être une combinaison des constantes **dbRepMakeReadOnly** et **dbRepMakePartial**, ou il peut être 0.</span><span class="sxs-lookup"><span data-stu-id="c8884-130">The intOptions argument can be a combination of the constants **dbRepMakeReadOnly** and **dbRepMakePartial**, or it can be 0.</span></span> <span data-ttu-id="c8884-131">Par exemple, pour créer un réplica partiel en lecture seule, vous devez transmettre la valeur **dbRepMakeReadOnly** + **dbRepMakePartial** en tant que valeur d’Optionsint.</span><span class="sxs-lookup"><span data-stu-id="c8884-131">For example, to create a read-only partial replica, you should pass the value **dbRepMakeReadOnly** + **dbRepMakePartial** as the value of intOptions.</span></span>

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

