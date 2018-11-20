---
title: Propriété Recordset.RecordsetType (DAO)
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
ms.openlocfilehash: e4babfce754ec0e9c4744142570054c0249936f8
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026210"
---
# <a name="recordsetrecordsettype-property-dao"></a><span data-ttu-id="076f3-102">Propriété Recordset.RecordsetType (DAO)</span><span class="sxs-lookup"><span data-stu-id="076f3-102">Recordset.RecordsetType property (DAO)</span></span>

<span data-ttu-id="076f3-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="076f3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="076f3-p101">La propriété **RecordsetType** permet de spécifier le genre de jeu d'enregistrement disponible pour un formulaire. Type de données **Byte** en lecture-écriture.</span><span class="sxs-lookup"><span data-stu-id="076f3-p101">You can use the **RecordsetType** property to specify what kind of recordset is made available to a form. Read/write **Byte**.</span></span>

## <a name="syntax"></a><span data-ttu-id="076f3-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="076f3-106">Syntax</span></span>

<span data-ttu-id="076f3-107">*expression* . RecordsetType</span><span class="sxs-lookup"><span data-stu-id="076f3-107">*expression* .RecordsetType</span></span>

<span data-ttu-id="076f3-108">*expression* Une variable qui représente un objet **Form**.</span><span class="sxs-lookup"><span data-stu-id="076f3-108">*expression* A variable that represents a **Form** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="076f3-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="076f3-109">Remarks</span></span>

<span data-ttu-id="076f3-110">La propriété **RecordsetType** utilise les paramètres suivants dans une base de données Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="076f3-110">The **RecordsetType** property uses the following settings in a Microsoft Access database.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="076f3-111">Paramètre</span><span class="sxs-lookup"><span data-stu-id="076f3-111">Setting</span></span></p></th>
<th><p><span data-ttu-id="076f3-112">Type de jeu d'enregistrement</span><span class="sxs-lookup"><span data-stu-id="076f3-112">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="076f3-113">Description</span><span class="sxs-lookup"><span data-stu-id="076f3-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="076f3-114">0</span><span class="sxs-lookup"><span data-stu-id="076f3-114">0</span></span></p></td>
<td><p><span data-ttu-id="076f3-115">Feuille de réponse dynamique</span><span class="sxs-lookup"><span data-stu-id="076f3-115">Dynaset</span></span></p></td>
<td><p><span data-ttu-id="076f3-116">(Valeur par défaut) Vous pouvez modifier les contrôles dépendants basés sur une seule table ou des tables avec une relation.</span><span class="sxs-lookup"><span data-stu-id="076f3-116">(Default) You can edit bound controls based on a single table or tables with a one-to-one relationship.</span></span> <span data-ttu-id="076f3-117">Pour les contrôles liés à des champs basés sur des tables avec une relation un-à-plusieurs, vous ne pouvez pas modifier les données du champ sur la &quot;un&quot; côté de la relation, sauf si la mise à jour en cascade est activée entre les tables.</span><span class="sxs-lookup"><span data-stu-id="076f3-117">For controls bound to fields based on tables with a one-to-many relationship, you can't edit data from the join field on the &quot;one&quot; side of the relationship unless cascade update is enabled between the tables.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076f3-118">1</span><span class="sxs-lookup"><span data-stu-id="076f3-118">1</span></span></p></td>
<td><p><span data-ttu-id="076f3-119">Feuille rép.dyn.(MAJ globale)</span><span class="sxs-lookup"><span data-stu-id="076f3-119">Dynaset (Inconsistent Updates)</span></span></p></td>
<td><p><span data-ttu-id="076f3-120">Toutes les tables et tous les contrôles correspondant à leurs champs peuvent être édités.</span><span class="sxs-lookup"><span data-stu-id="076f3-120">All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="076f3-121">2</span><span class="sxs-lookup"><span data-stu-id="076f3-121">2</span></span></p></td>
<td><p><span data-ttu-id="076f3-122">Instantané</span><span class="sxs-lookup"><span data-stu-id="076f3-122">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="076f3-123">Aucune table ou aucun contrôle correspondant à leurs champs ne peut être édité.</span><span class="sxs-lookup"><span data-stu-id="076f3-123">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="076f3-124">[!REMARQUE] Si vous ne voulez pas que les données des contrôles dépendants soient modifiées quand un formulaire est en mode Formulaire ou en mode Feuille de données, vous pouvez définir la propriété **RecordsetType** sur 2.</span><span class="sxs-lookup"><span data-stu-id="076f3-124">If you don't want data in bound controls to be edited when a form is in Form view or Datasheet view, you can set the **RecordsetType** property to 2.</span></span>

<span data-ttu-id="076f3-125">Dans un projet Microsoft Access (.adp), la propriété **RecordsetType** utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="076f3-125">The **RecordsetType** property uses the following settings in a Microsoft Access project (.adp).</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="076f3-126">Paramètre</span><span class="sxs-lookup"><span data-stu-id="076f3-126">Setting</span></span></p></th>
<th><p><span data-ttu-id="076f3-127">Type de jeu d'enregistrement</span><span class="sxs-lookup"><span data-stu-id="076f3-127">Type of Recordset</span></span></p></th>
<th><p><span data-ttu-id="076f3-128">Description</span><span class="sxs-lookup"><span data-stu-id="076f3-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="076f3-129">3</span><span class="sxs-lookup"><span data-stu-id="076f3-129">3</span></span></p></td>
<td><p><span data-ttu-id="076f3-130">Instantané</span><span class="sxs-lookup"><span data-stu-id="076f3-130">Snapshot</span></span></p></td>
<td><p><span data-ttu-id="076f3-131">Aucune table ou aucun contrôle correspondant à leurs champs ne peut être édité.</span><span class="sxs-lookup"><span data-stu-id="076f3-131">No tables or the controls bound to their fields can be edited.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="076f3-132">4</span><span class="sxs-lookup"><span data-stu-id="076f3-132">4</span></span></p></td>
<td><p><span data-ttu-id="076f3-133">Possibilité de mise à jour de l'instantané</span><span class="sxs-lookup"><span data-stu-id="076f3-133">Updatable Snapshot</span></span></p></td>
<td><p><span data-ttu-id="076f3-134">(Valeur par défaut) Toutes les tables et tous les contrôles correspondant à leurs champs peuvent être édités.</span><span class="sxs-lookup"><span data-stu-id="076f3-134">(Default) All tables and controls bound to their fields can be edited.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="076f3-135">[!REMARQUE] Toute modification de la propriété **RecordsetType** d'un état ou d'un formulaire ouvert entraîne la recréation automatique d'un jeu d'enregistrements.</span><span class="sxs-lookup"><span data-stu-id="076f3-135">Changing the **RecordsetType** property of an open form or report causes an automatic recreation of the recordset.</span></span>

<span data-ttu-id="076f3-p103">Vous pouvez créer des formulaires basés sur des tables sous-jacentes multiples avec des champs correspondants à des contrôles dans les formulaires. En fonction du paramètre de la propriété **RecordsetType**, vous pouvez choisir lesquels de ces contrôles dépendants pourront être édités.</span><span class="sxs-lookup"><span data-stu-id="076f3-p103">You can create forms based on multiple underlying tables with fields bound to controls on the forms. Depending on the **RecordsetType** property setting, you can limit which of these bound controls can be edited.</span></span>

<span data-ttu-id="076f3-138">Outre le contrôle d’édition fourni par la **propriété RecordsetType**, chaque contrôle d’un formulaire a une propriété **Locked** que vous pouvez définir pour spécifier si le contrôle et ses données sous-jacentes peuvent être modifiés.</span><span class="sxs-lookup"><span data-stu-id="076f3-138">In addition to the editing control provided by **RecordsetType**, each control on a form has a **Locked** property that you can set to specify whether the control and its underlying data can be edited.</span></span> <span data-ttu-id="076f3-139">Si la propriété **Locked** est définie sur Oui, vous ne pouvez pas modifier les données.</span><span class="sxs-lookup"><span data-stu-id="076f3-139">If the **Locked** property is set to Yes, you can't edit the data.</span></span>

## <a name="example"></a><span data-ttu-id="076f3-140">Exemple</span><span class="sxs-lookup"><span data-stu-id="076f3-140">Example</span></span>

<span data-ttu-id="076f3-p105">Dans l'exemple suivant, seul un utilisateur dont l'ID est ADMIN peut mettre à jour des enregistrements. Cet exemple de code définit la propriété **RecordsetType** sur Instantané si la valeur de la variable publique gstrUserID n'est pas ADMIN.</span><span class="sxs-lookup"><span data-stu-id="076f3-p105">In the following example, only if the user ID is ADMIN can records be updated. This code sample sets the **RecordsetType** property to Snapshot if the public variable gstrUserID value is not ADMIN.</span></span>

```vb
    Sub Form_Open(Cancel As Integer) 
     Const conSnapshot = 2 
     If gstrUserID <> "ADMIN" Then 
     Forms!Employees.RecordsetType = conSnapshot 
     End If 
    End Sub
```

## <a name="see-also"></a><span data-ttu-id="076f3-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="076f3-143">See also</span></span>

- [<span data-ttu-id="076f3-144">Form, objet</span><span class="sxs-lookup"><span data-stu-id="076f3-144">Form Object</span></span>](https://docs.microsoft.com/office/vba/api/Access.Form)


