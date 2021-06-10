---
title: Recordset.RecordsetType, propriété (DAO)
TOCTitle: RecordsetType Property
ms:assetid: a66d4043-08cc-ead1-f9ff-efc7d7ea21bf
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821178(v=office.15)
ms:contentKeyID: 48546853
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm13361
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 64f7dda8bec7806ef510d265deab350dc3cdad6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307629"
---
# <a name="recordsetrecordsettype-property-dao"></a><span data-ttu-id="82f8b-102">Recordset.RecordsetType, propriété (DAO)</span><span class="sxs-lookup"><span data-stu-id="82f8b-102">Recordset.RecordsetType property (DAO)</span></span>

<span data-ttu-id="82f8b-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82f8b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82f8b-p101">La propriété **RecordsetType** permet de spécifier le genre de jeu d'enregistrement disponible pour un formulaire. Type de données **Byte** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="82f8b-p101">You can use the **RecordsetType** property to specify what kind of recordset is made available to a form. Read/write **Byte**.</span></span>

## <a name="syntax"></a><span data-ttu-id="82f8b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82f8b-106">Syntax</span></span>

<span data-ttu-id="82f8b-107">*.* RecordsetType</span><span class="sxs-lookup"><span data-stu-id="82f8b-107">*expression* .RecordsetType</span></span>

<span data-ttu-id="82f8b-108">*expression* Variable qui représente un objet **Form**.</span><span class="sxs-lookup"><span data-stu-id="82f8b-108">*expression* A variable that represents a **Form** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="82f8b-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="82f8b-109">Remarks</span></span>

<span data-ttu-id="82f8b-110">La propriété **RecordsetType** utilise les paramètres suivants dans une base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="82f8b-110">The **RecordsetType** property uses the following settings in a Microsoft Access database.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82f8b-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="82f8b-111">Setting</span></span></p></th>
<th><p><span data-ttu-id="82f8b-112">Type de jeu d'enregistrement</span><span class="sxs-lookup"><span data-stu-id="82f8b-112">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="82f8b-113">Description</span><span class="sxs-lookup"><span data-stu-id="82f8b-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82f8b-114">0</span><span class="sxs-lookup"><span data-stu-id="82f8b-114">0</span></span></p></td>
<td><p><span data-ttu-id="82f8b-115">Feuille deynaset</span><span class="sxs-lookup"><span data-stu-id="82f8b-115">Dynaset</span></span></p></td>
<td><p><span data-ttu-id="82f8b-116">(Valeur par défaut) Vous pouvez modifier des contrôles dépendants basés sur une seule ou plusieurs tables avec une relation un-à-un.</span><span class="sxs-lookup"><span data-stu-id="82f8b-116">(Default) You can edit bound controls based on a single table or tables with a one-to-one relationship.</span></span> <span data-ttu-id="82f8b-117">Pour les contrôles liés à des champs basés sur des tables avec une relation un-à-plusieurs, vous ne pouvez pas modifier les données du champ joint du côté un de la relation, sauf si la mise à jour en cascade est activée entre les &quot; &quot; tables.</span><span class="sxs-lookup"><span data-stu-id="82f8b-117">For controls bound to fields based on tables with a one-to-many relationship, you can't edit data from the join field on the &quot;one&quot; side of the relationship unless cascade update is enabled between the tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f8b-118">1</span><span class="sxs-lookup"><span data-stu-id="82f8b-118">1</span></span></p></td>
<td><p><span data-ttu-id="82f8b-119">Feuille rép.dyn.(MAJ globale)</span><span class="sxs-lookup"><span data-stu-id="82f8b-119">Dynaset (Inconsistent Updates)</span></span></p></td>
<td><p><span data-ttu-id="82f8b-120">Toutes les tables et tous les contrôles correspondant à leurs champs peuvent être édités.</span><span class="sxs-lookup"><span data-stu-id="82f8b-120">All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82f8b-121">2</span><span class="sxs-lookup"><span data-stu-id="82f8b-121">2</span></span></p></td>
<td><p><span data-ttu-id="82f8b-122">Capture instantanée</span><span class="sxs-lookup"><span data-stu-id="82f8b-122">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="82f8b-123">Aucune table ou aucun contrôle correspondant à leurs champs ne peut être édité.</span><span class="sxs-lookup"><span data-stu-id="82f8b-123">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="82f8b-124">[!REMARQUE] Si vous ne voulez pas que les données des contrôles dépendants soient modifiées quand un formulaire est en mode Formulaire ou en mode Feuille de données, vous pouvez définir la propriété **RecordsetType** sur 2.</span><span class="sxs-lookup"><span data-stu-id="82f8b-124">If you don't want data in bound controls to be edited when a form is in Form view or Datasheet view, you can set the **RecordsetType** property to 2.</span></span>

<span data-ttu-id="82f8b-125">Dans un projet Microsoft Access (.adp), la propriété **RecordsetType** utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="82f8b-125">The **RecordsetType** property uses the following settings in a Microsoft Access project (.adp).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="82f8b-126">Paramètre</span><span class="sxs-lookup"><span data-stu-id="82f8b-126">Setting</span></span></p></th>
<th><p><span data-ttu-id="82f8b-127">Type de jeu d'enregistrement</span><span class="sxs-lookup"><span data-stu-id="82f8b-127">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="82f8b-128">Description</span><span class="sxs-lookup"><span data-stu-id="82f8b-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82f8b-129">3</span><span class="sxs-lookup"><span data-stu-id="82f8b-129">3</span></span></p></td>
<td><p><span data-ttu-id="82f8b-130">Capture instantanée</span><span class="sxs-lookup"><span data-stu-id="82f8b-130">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="82f8b-131">Aucune table ou aucun contrôle correspondant à leurs champs ne peut être édité.</span><span class="sxs-lookup"><span data-stu-id="82f8b-131">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82f8b-132">4 </span><span class="sxs-lookup"><span data-stu-id="82f8b-132">4</span></span></p></td>
<td><p><span data-ttu-id="82f8b-133">Possibilité de mise à jour de l'instantané</span><span class="sxs-lookup"><span data-stu-id="82f8b-133">Updatable Snapshot</span></span></p></td>
<td><p><span data-ttu-id="82f8b-134">(Valeur par défaut) Toutes les tables et tous les contrôles correspondant à leurs champs peuvent être édités.</span><span class="sxs-lookup"><span data-stu-id="82f8b-134">(Default) All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="82f8b-135">[!REMARQUE] Toute modification de la propriété **RecordsetType** d'un état ou d'un formulaire ouvert entraîne la recréation automatique d'un jeu d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="82f8b-135">Changing the **RecordsetType** property of an open form or report causes an automatic recreation of the recordset.</span></span>

<span data-ttu-id="82f8b-p103">Vous pouvez créer des formulaires basés sur des tables sous-jacentes multiples avec des champs correspondants à des contrôles dans les formulaires. En fonction du paramètre de la propriété **RecordsetType**, vous pouvez choisir lesquels de ces contrôles dépendants pourront être édités.</span><span class="sxs-lookup"><span data-stu-id="82f8b-p103">You can create forms based on multiple underlying tables with fields bound to controls on the forms. Depending on the **RecordsetType** property setting, you can limit which of these bound controls can be edited.</span></span>

<span data-ttu-id="82f8b-138">Outre le contrôle d’édition fourni par **RecordsetType,** chaque contrôle d’un formulaire possède une propriété **Locked** que vous pouvez définir pour spécifier si le contrôle et ses données sous-jacentes peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="82f8b-138">In addition to the editing control provided by **RecordsetType**, each control on a form has a **Locked** property that you can set to specify whether the control and its underlying data can be edited.</span></span> <span data-ttu-id="82f8b-139">Si la propriété **Locked** est définie sur Oui, vous ne pouvez pas modifier les données.</span><span class="sxs-lookup"><span data-stu-id="82f8b-139">If the **Locked** property is set to Yes, you can't edit the data.</span></span>

## <a name="example"></a><span data-ttu-id="82f8b-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="82f8b-140">Example</span></span>

<span data-ttu-id="82f8b-p105">Dans l'exemple suivant, seul un utilisateur dont l'ID est ADMIN peut mettre à jour des enregistrements. Cet exemple de code définit la propriété **RecordsetType** sur Instantané si la valeur de la variable publique gstrUserID n'est pas ADMIN.</span><span class="sxs-lookup"><span data-stu-id="82f8b-p105">In the following example, only if the user ID is ADMIN can records be updated. This code sample sets the **RecordsetType** property to Snapshot if the public variable gstrUserID value is not ADMIN.</span></span>

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a><span data-ttu-id="82f8b-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82f8b-143">See also</span></span>

- [<span data-ttu-id="82f8b-144">Form, objet</span><span class="sxs-lookup"><span data-stu-id="82f8b-144">Form Object</span></span>](https://docs.microsoft.com/office/vba/api/Access.Form)


