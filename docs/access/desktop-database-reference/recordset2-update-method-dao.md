---
title: Recordset2.Update, méthode (DAO)
TOCTitle: Update Method
ms:assetid: 1b47606a-e79c-23f1-b120-46d1429bc167
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845700(v=office.15)
ms:contentKeyID: 48543537
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052882
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4259da0eb48e7ff13e246b326cc6e96d7a916ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307167"
---
# <a name="recordset2update-method-dao"></a><span data-ttu-id="d4c38-102">Recordset2.Update, méthode (DAO)</span><span class="sxs-lookup"><span data-stu-id="d4c38-102">Recordset2.Update method (DAO)</span></span>

<span data-ttu-id="d4c38-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d4c38-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c38-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4c38-104">Syntax</span></span>

<span data-ttu-id="d4c38-105">*expression* .Update(***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="d4c38-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="d4c38-106">*expression* Variable qui représente un **objet Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="d4c38-106">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d4c38-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d4c38-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d4c38-108">Nom</span><span class="sxs-lookup"><span data-stu-id="d4c38-108">Name</span></span></p></th>
<th><p><span data-ttu-id="d4c38-109">Obligatoire/facultatif</span><span class="sxs-lookup"><span data-stu-id="d4c38-109">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d4c38-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="d4c38-110">Data type</span></span></p></th>
<th><p><span data-ttu-id="d4c38-111">Description</span><span class="sxs-lookup"><span data-stu-id="d4c38-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d4c38-112"><em>UpdateType</em></span><span class="sxs-lookup"><span data-stu-id="d4c38-112"><em>UpdateType</em></span></span></p></td>
<td><p><span data-ttu-id="d4c38-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d4c38-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="d4c38-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="d4c38-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="d4c38-115">A <strong> <a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a> </strong> constante indiquant le type de mise à jour, comme spécifié dans les paramètres (espaces).</span><span class="sxs-lookup"><span data-stu-id="d4c38-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d4c38-116"><em>Force</em></span><span class="sxs-lookup"><span data-stu-id="d4c38-116"><em>Force</em></span></span></p></td>
<td><p><span data-ttu-id="d4c38-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="d4c38-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="d4c38-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="d4c38-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="d4c38-119">Valeur <strong>booléenne</strong> indiquant si les modifications doivent être forcées ou non dans la base de données, indépendamment du fait que les données sous-jacentes aient été modifiées par un autre utilisateur depuis l'appel de <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="d4c38-119">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call.</span></span> <span data-ttu-id="d4c38-120">Si la valeur est <strong>True</strong>, les modifications sont forcées et les modifications apportées par d'autres utilisateurs sont tout simplement remplacées.</span><span class="sxs-lookup"><span data-stu-id="d4c38-120">If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten.</span></span> <span data-ttu-id="d4c38-121">Si la valeur est <strong>False</strong> (valeur par défaut), les modifications apportées par d'autres utilisateurs tandis que la mise à jour est en attente entraîneront l'échec de la mise à jour pour les modifications en conflit.</span><span class="sxs-lookup"><span data-stu-id="d4c38-121">If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict.</span></span> <span data-ttu-id="d4c38-122">Aucune erreur ne se produit, mais les propriétés <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> et <strong>BatchCollisions</strong> indiquent respectivement le nombre de conflits et les lignes affectées par les conflits (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="d4c38-122">No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="d4c38-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="d4c38-123">Remarks</span></span>

<span data-ttu-id="d4c38-124">Utilisez **mise à jour** pour enregistrer l’enregistrement actif et toutes les modifications apportées à celui-ci.</span><span class="sxs-lookup"><span data-stu-id="d4c38-124">Use **Update** to save the current record and any changes you've made to it.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d4c38-125">Enregistrer les modifications apportées à l’enregistrement actif</span><span class="sxs-lookup"><span data-stu-id="d4c38-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="d4c38-126">Vous utilisez le **modifier** ou **AddNew** méthode, puis accéder à un autre enregistrement sans utiliser première **mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="d4c38-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="d4c38-127">Vous utilisez **modifier** ou **AddNew**, puis utilisez **modifier** ou **AddNew** nouveau sans utiliser première **mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="d4c38-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="d4c38-128">Vous définissez la **[signet](recordset2-bookmark-property-dao.md)** propriété vers un autre enregistrement.</span><span class="sxs-lookup"><span data-stu-id="d4c38-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="d4c38-129">Vous fermez le **jeu d’enregistrements** sans utiliser première **mise à jour**.</span><span class="sxs-lookup"><span data-stu-id="d4c38-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="d4c38-130">Vous annulez la **modifier** opération à l’aide **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d4c38-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="d4c38-p102">Pour modifier un enregistrement, utilisez la **modifier** méthode pour copier le contenu de l’enregistrement actif dans la mémoire tampon de copie. Si vous n’utilisez **modifier** tout d’abord, une erreur se produit lorsque vous utilisez **mise à jour** ou tenter de modifier la valeur du champ.</span><span class="sxs-lookup"><span data-stu-id="d4c38-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="d4c38-133">Dans un espace de travail ODBCDirect, vous pouvez effectuer par lot mises à jour, sous réserve la bibliothèque curseur prend en charge les mises à jour du lot et le **jeu d’enregistrements** a été ouvert avec l’option de verrouillage par lot optimiste.</span><span class="sxs-lookup"><span data-stu-id="d4c38-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="d4c38-134">Dans un espace de travail Microsoft Access, lorsque le **jeu d’enregistrements** d’objet **LockEdits** paramètre de la propriété est **vrai** (verrouillage pessimiste) dans un environnement multi-utilisateurs, l’enregistrement reste verrouillé à partir du moment **modifier** sert jusqu'à ce que le **mise à jour** méthode est exécutée ou la modification est annulée.</span><span class="sxs-lookup"><span data-stu-id="d4c38-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="d4c38-135">Si le **LockEdits** paramètre de la propriété est **faux** (verrouillage optimiste), l’enregistrement est verrouillé et par rapport à l’enregistrement déjà modifiée juste avant qu’il est mis à jour dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="d4c38-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="d4c38-136">Si l’enregistrement a changé, car vous avez utilisé le **modifier** méthode, le **mise à jour** opération échoue.</span><span class="sxs-lookup"><span data-stu-id="d4c38-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="d4c38-137">Base de données Microsoft Access connectées moteur ODBC et bases de données ISAM toujours utilisent le verrouillage optimiste.</span><span class="sxs-lookup"><span data-stu-id="d4c38-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="d4c38-138">Pour continuer la **mise à jour** opération avec vos modifications, utilisez la **mise à jour** méthode nouveau.</span><span class="sxs-lookup"><span data-stu-id="d4c38-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="d4c38-139">Pour revenir à l’enregistrement tel que l’autre utilisateur l’a modifié, actualisez l’enregistrement actif à l’aide de la commande Move 0.</span><span class="sxs-lookup"><span data-stu-id="d4c38-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>

> [!NOTE]
> <span data-ttu-id="d4c38-p104">Pour ajouter, modifier ou supprimer un enregistrement, il doit y avoir un index unique sur l’enregistrement dans la source de données sous-jacentes. Si non, une erreur « Autorisation refusée » doit se produire sur le **AddNew**, **supprimer**, ou **modifier** méthode appel dans un espace de travail Microsoft Access ou une erreur « Argument non valide » se produit sur la **mise à jour** appeler dans un espace de travail ODBCDirect.</span><span class="sxs-lookup"><span data-stu-id="d4c38-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>


