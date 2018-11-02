---
title: Méthode Recordset2.Update (DAO)
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
ms.openlocfilehash: 64b758272d968ac5f276aa89c448215dee32b86f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923460"
---
# <a name="recordset2update-method-dao"></a><span data-ttu-id="61a96-102">Méthode Recordset2.Update (DAO)</span><span class="sxs-lookup"><span data-stu-id="61a96-102">Recordset2.Update method (DAO)</span></span>


<span data-ttu-id="61a96-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="61a96-103">**Applies to**: Access 2013, Office 2013</span></span>

## <a name="syntax"></a><span data-ttu-id="61a96-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="61a96-104">Syntax</span></span>

<span data-ttu-id="61a96-105">*expression* . Mise à jour (***UpdateType***, ***Force***)</span><span class="sxs-lookup"><span data-stu-id="61a96-105">*expression* .Update(***UpdateType***, ***Force***)</span></span>

<span data-ttu-id="61a96-106">*expression* Variable qui représente un objet **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="61a96-106">*expression* A variable that represents a **Recordset2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="61a96-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="61a96-107">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="61a96-108">Name</span><span class="sxs-lookup"><span data-stu-id="61a96-108">Name</span></span></p></th>
<th><p><span data-ttu-id="61a96-109">Obligatoire/Facultatif</span><span class="sxs-lookup"><span data-stu-id="61a96-109">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="61a96-110">Type de données</span><span class="sxs-lookup"><span data-stu-id="61a96-110">Data Type</span></span></p></th>
<th><p><span data-ttu-id="61a96-111">Description</span><span class="sxs-lookup"><span data-stu-id="61a96-111">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61a96-112">UpdateType</span><span class="sxs-lookup"><span data-stu-id="61a96-112">UpdateType</span></span></p></td>
<td><p><span data-ttu-id="61a96-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="61a96-113">Optional</span></span></p></td>
<td><p><span data-ttu-id="61a96-114"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="61a96-114"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="61a96-115">Constante <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> qui indique le type de mise à jour, comme spécifié dans les paramètres (espaces de travail ODBCDirect uniquement).</span><span class="sxs-lookup"><span data-stu-id="61a96-115">A <strong><a href="updatetypeenum-enumeration-dao.md">UpdateTypeEnum</a></strong> constant indicating the type of update, as specified in Settings (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61a96-116">Force</span><span class="sxs-lookup"><span data-stu-id="61a96-116">Force</span></span></p></td>
<td><p><span data-ttu-id="61a96-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="61a96-117">Optional</span></span></p></td>
<td><p><span data-ttu-id="61a96-118"><strong>Boolean</strong></span><span class="sxs-lookup"><span data-stu-id="61a96-118"><strong>Boolean</strong></span></span></p></td>
<td><p><span data-ttu-id="61a96-p101">Valeur <strong>booléenne</strong> indiquant si les modifications doivent être forcées ou non dans la base de données, indépendamment du fait que les données sous-jacentes aient été modifiées par un autre utilisateur depuis l'appel de <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong> ou <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong>. Si la valeur est <strong>True</strong>, les modifications sont forcées et les modifications apportées par d'autres utilisateurs sont tout simplement remplacées. Si la valeur est <strong>False</strong> (valeur par défaut), les modifications apportées par d'autres utilisateurs tandis que la mise à jour est en attente entraîneront l'échec de la mise à jour pour les modifications en conflit. Aucune erreur ne se produit, mais les propriétés <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> et <strong>BatchCollisions</strong> indiqueront le nombre de conflits et les lignes concernées par ces conflits, respectivement (espaces de travail ODBCDirect uniquement).  </span><span class="sxs-lookup"><span data-stu-id="61a96-p101">A <strong>Boolean</strong> value indicating whether or not to force the changes into the database, regardless of whether the underlying data has been changed by another user since the <strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong>, <strong><a href="fields-delete-method-dao.md">Delete</a></strong>, or <strong><a href="recordset2-edit-method-dao.md">Edit</a></strong> call. If <strong>True</strong>, the changes are forced and changes made by other users are simply overwritten. If <strong>False</strong> (default), changes made by another user while the update is pending will cause the update to fail for those changes that are in conflict. No error occurs, but the <strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong> and <strong>BatchCollisions</strong> properties will indicate the number of conflicts and the rows affected by conflicts, respectively (ODBCDirect workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="61a96-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="61a96-123">Remarks</span></span>

<span data-ttu-id="61a96-124">Utilisez la méthode **Update** pour enregistrer l'enregistrement actif et les modifications que vous y avez effectuées.</span><span class="sxs-lookup"><span data-stu-id="61a96-124">Use **Update** to save the current record and any changes you've made to it.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="61a96-125">[!IMPORTANTE] Les modifications apportées à l'enregistrement actif sont perdues dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="61a96-125">Changes to the current record are lost if:</span></span>
> - <span data-ttu-id="61a96-126">vous utilisez la méthode **Edit** ou **AddNew** et passez à un autre enregistrement sans utiliser au préalable la méthode **Update**;</span><span class="sxs-lookup"><span data-stu-id="61a96-126">You use the **Edit** or **AddNew** method, and then move to another record without first using **Update**.</span></span>
> - <span data-ttu-id="61a96-127">vous utilisez la méthode **Edit** ou **AddNew**, puis vous réutilisez la méthode **Edit** ou **AddNew** sans utiliser au préalable la méthode **Update**</span><span class="sxs-lookup"><span data-stu-id="61a96-127">You use **Edit** or **AddNew**, and then use **Edit** or **AddNew** again without first using **Update**.</span></span>
> - <span data-ttu-id="61a96-128">vous affectez la propriété **[Bookmark](recordset2-bookmark-property-dao.md)** à un autre enregistrement ;</span><span class="sxs-lookup"><span data-stu-id="61a96-128">You set the **[Bookmark](recordset2-bookmark-property-dao.md)** property to another record.</span></span>
> - <span data-ttu-id="61a96-129">vous fermez l'objet **Recordset** sans utiliser au préalable la méthode **Update**;</span><span class="sxs-lookup"><span data-stu-id="61a96-129">You close the **Recordset** without first using **Update**.</span></span>
> - <span data-ttu-id="61a96-130">vous annulez l'opération **Edit** par le biais de la méthode **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="61a96-130">You cancel the **Edit** operation by using **[CancelUpdate](recordset2-cancelupdate-method-dao.md)**.</span></span>

<span data-ttu-id="61a96-p102">Pour modifier un enregistrement, utilisez la méthode **Edit** pour copier le contenu de l'enregistrement actif dans la mémoire tampon de la copie. Si vous n'utilisez pas d'abord la méthode **Edit**, une erreur se produit lorsque vous utilisez **Update** ou que vous tentez de modifier la valeur d'un champ.</span><span class="sxs-lookup"><span data-stu-id="61a96-p102">To edit a record, use the **Edit** method to copy the contents of the current record to the copy buffer. If you don't use **Edit** first, an error occurs when you use **Update** or attempt to change a field's value.</span></span>

<span data-ttu-id="61a96-133">Dans un espace de travail ODBCDirect, vous pouvez effectuer des mises à jour par lot, à condition que la bibliothèque de curseurs prenne en charge ce type d'opération et que l'objet **Recordset** ait été ouvert avec l'option de verrouillage par lot optimiste.</span><span class="sxs-lookup"><span data-stu-id="61a96-133">In an ODBCDirect workspace, you can do batch updates, provided the cursor library supports batch updates, and the **Recordset** was opened with the optimistic batch locking option.</span></span>

<span data-ttu-id="61a96-134">Dans un espace de travail Microsoft Access, lorsque la propriété **LockEdits** de l'objet **Recordset** a la valeur **True** (verrouillage pessimiste) dans un environnement multi-utilisateur, l'enregistrement reste verrouillé du moment où la méthode **Edit** est utilisée jusqu'à l'exécution de la méthode **Update** ou l'annulation de la modification.</span><span class="sxs-lookup"><span data-stu-id="61a96-134">In a Microsoft Access workspace, when the **Recordset** object's **LockEdits** property setting is **True** (pessimistically locked) in a multiuser environment, the record remains locked from the time **Edit** is used until the **Update** method is executed or the edit is canceled.</span></span> <span data-ttu-id="61a96-135">Si la propriété **LockEdits** a la valeur **False** (verrouillage optimiste), l'enregistrement est verrouillé et comparé à l'enregistrement tel qu'il était avant sa modification juste avant sa mise à jour dans la base de données.</span><span class="sxs-lookup"><span data-stu-id="61a96-135">If the **LockEdits** property setting is **False** (optimistically locked), the record is locked and compared with the pre-edited record just before it is updated in the database.</span></span> <span data-ttu-id="61a96-136">Si l'enregistrement a changé depuis l'utilisation de la méthode **Edit**, l'opération **Update** échoue.</span><span class="sxs-lookup"><span data-stu-id="61a96-136">If the record has changed since you used the **Edit** method, the **Update** operation fails.</span></span> <span data-ttu-id="61a96-137">Les bases de données ODBC et ISAM installables connectées au moteur de base de données Microsoft Access utilisent toujours un verrouillage optimiste.</span><span class="sxs-lookup"><span data-stu-id="61a96-137">Microsoft Access database engine-connected ODBC and installable ISAM databases always use optimistic locking.</span></span> <span data-ttu-id="61a96-138">Pour poursuivre l'opération **Update** avec vos modifications, utilisez à nouveau la méthode **Update**.</span><span class="sxs-lookup"><span data-stu-id="61a96-138">To continue the **Update** operation with your changes, use the **Update** method again.</span></span> <span data-ttu-id="61a96-139">Pour revenir à l’enregistrement en tant que l’autre utilisateur l’avait modifié, actualisez l’enregistrement actif en utilisant Move 0.</span><span class="sxs-lookup"><span data-stu-id="61a96-139">To revert to the record as the other user changed it, refresh the current record by using Move 0.</span></span>


> [!NOTE]
> <span data-ttu-id="61a96-p104">[!REMARQUE] Pour ajouter, modifier ou supprimer un enregistrement, un index unique doit exister au niveau de l'enregistrement de la source de données sous-jacente. À défaut, une erreur de type « Autorisation refusée » se produit consécutivement à l'appel d'une méthode **Update**, **Edit** ou **AddNew** dans un espace de travail Microsoft Access ; dans un espace de travail ODBCDirect, l'appel de **Delete** provoque une erreur de type « Argument incorrect ».</span><span class="sxs-lookup"><span data-stu-id="61a96-p104">To add, edit, or delete a record, there must be a unique index on the record in the underlying data source. If not, a "Permission denied" error will occur on the **AddNew**, **Delete**, or **Edit** method call in a Microsoft Access workspace, or an "Invalid argument" error will occur on the **Update** call in an ODBCDirect workspace.</span></span>


