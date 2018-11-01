---
title: DéfinirPropriété, action de macro
TOCTitle: SetProperty Macro Action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
ms.openlocfilehash: ac0cb0fe608ad5f3e15ae72346eac30628ba3dfa
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25887382"
---
# <a name="setproperty-macro-action"></a><span data-ttu-id="3eafc-102">DéfinirPropriété, action de macro</span><span class="sxs-lookup"><span data-stu-id="3eafc-102">SetProperty Macro Action</span></span>

<span data-ttu-id="3eafc-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3eafc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3eafc-104">L'action **DéfinirPropriété** permet de définir une propriété pour un contrôle dans un formulaire ou un état.</span><span class="sxs-lookup"><span data-stu-id="3eafc-104">You can use the **SetProperty** action to set a property for a control on a form or a report.</span></span>

## <a name="setting"></a><span data-ttu-id="3eafc-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eafc-105">Setting</span></span>

<span data-ttu-id="3eafc-106">L'action **DéfinirPropriété** utilise les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3eafc-106">The **SetProperty** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3eafc-107">Argument de l’action</span><span class="sxs-lookup"><span data-stu-id="3eafc-107">Action argument</span></span></p></th>
<th><p><span data-ttu-id="3eafc-108">Description</span><span class="sxs-lookup"><span data-stu-id="3eafc-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-109">Nom du contrôle</span><span class="sxs-lookup"><span data-stu-id="3eafc-109">Control Name</span></span></p></td>
<td><p><span data-ttu-id="3eafc-110">Tapez le nom du champ ou du contrôle pour lequel vous voulez définir la valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="3eafc-110">Type the name of the field or control for which you want to set the property value.</span></span> <span data-ttu-id="3eafc-111">Utilisez uniquement le nom de contrôle, et non la syntaxe complète.</span><span class="sxs-lookup"><span data-stu-id="3eafc-111">Use only the control name, not the full syntax.</span></span> <span data-ttu-id="3eafc-112">Laissez cet argument vide si vous souhaitez définir cette propriété pour le formulaire ou l'état actif.</span><span class="sxs-lookup"><span data-stu-id="3eafc-112">Leave this argument blank to set the property for the current form or report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3eafc-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="3eafc-113">Property</span></span></p></td>
<td><p><span data-ttu-id="3eafc-p102">Sélectionnez la propriété dont la valeur doit être définie. Consultez la section <strong>Remarques</strong> de cet article pour accéder à la liste des propriétés qui peuvent être définies via cette action.</span><span class="sxs-lookup"><span data-stu-id="3eafc-p102">Select the property that you want to set. See the <strong>Remarks</strong> section in this article for a list of the properties that can be set by using this action.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3eafc-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3eafc-116">Value</span></span></p></td>
<td><p><span data-ttu-id="3eafc-p103">Tapez la valeur que vous souhaitez définir pour la propriété. Pour les propriétés dont la valeur doit être définie sur Oui ou Non, utilisez <strong>-1</strong> pour Oui et <strong>0</strong> pour Non.</span><span class="sxs-lookup"><span data-stu-id="3eafc-p103">Type the value that the property is to be set to. For properties whose values are either Yes or No, use <strong>-1</strong> for Yes and <strong>0</strong> for No.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="3eafc-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="3eafc-119">Remarks</span></span>

- <span data-ttu-id="3eafc-120">L'action **DéfinirPropriété** permet de définir les propriétés suivantes pour un contrôle : **Activé**, **Visible**, **Verrouillé**, **Gauche**, **Haut**, **Largeur**, **Hauteur**, **Couleur texte**, **Couleur fond** ou **Légende**.</span><span class="sxs-lookup"><span data-stu-id="3eafc-120">You can use the **SetProperty** action to set the following properties of a control: **Enabled**, **Visible**, **Locked**, **Left**, **Top**, **Width**, **Height**, **Fore Color**, **Back Color**, or **Caption**.</span></span>

- <span data-ttu-id="3eafc-121">Si vous entrez une valeur non admise pour l’argument ***Valeur***, aucune erreur ne se produit, mais il se peut que la valeur de la propriété soit modifiée dans Access, selon l’interprétation de l’argument.</span><span class="sxs-lookup"><span data-stu-id="3eafc-121">If you enter an invalid value for the ***Value*** argument, no error occurs, but Access might change the property to a different value, depending on how it interprets the argument.</span></span>

- <span data-ttu-id="3eafc-p104">L'action **DéfinirPropriété** peut être utilisée dans une macro autonome, à condition de la faire précéder d'une action sélectionnant le formulaire ou l'état contenant le contrôle pour lequel la propriété est définie. Si le formulaire ou l'état n'est pas ouvert, vous pouvez utiliser les actions **OuvrirFormulaire** ou **OuvrirEtat** pour l'ouvrir et le sélectionner. Si le formulaire ou l'état est déjà ouvert, vous pouvez utiliser l'action **SélectionnerObjet** pour le sélectionner. Vous pouvez ensuite utiliser l'action **DéfinirPropriété** pour définir la propriété. La sélection de l'objet n'est pas nécessaire si vous utilisez l'action **DéfinirPropriété** dans une macro incorporée dans un contrôle du même formulaire ou du même état que le contrôle pour lequel vous définissez la propriété.</span><span class="sxs-lookup"><span data-stu-id="3eafc-p104">You can use the **SetProperty** action in a stand-alone macro only if you precede it with an action that selects the form or report containing the control for which you are setting the property. If the form or report is not open, you can use the **OpenForm** or **OpenReport** action to open and select it. If the form or report is already open, you can use the **SelectObject** action to select it. You can then use the **SetProperty** action to set the property. Selecting the object is not necessary if you use the **SetProperty** action in a macro which is embedded in a control on the same form or report as the control for which you are setting the property.</span></span>

- <span data-ttu-id="3eafc-127">Pour exécuter l’action **DéfinirPropriété** dans un module VBA, utilisez la méthode \*\* DéfinirPropriété\*\* de l’objet **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="3eafc-127">To run the **SetProperty** action in a VBA module, use the **SetProperty** method of the **DoCmd** object.</span></span>

## <a name="example"></a><span data-ttu-id="3eafc-128">Exemple</span><span class="sxs-lookup"><span data-stu-id="3eafc-128">Example</span></span>

<span data-ttu-id="3eafc-129">L’exemple suivant montre comment utiliser l’action DéfinirPropriété pour faire basculer la visibilité de la zone de texte **MyTextBox** .</span><span class="sxs-lookup"><span data-stu-id="3eafc-129">The following example shows how to use the SetProperty action to toggle the visibility of the **MyTextBox** text box.</span></span>

<span data-ttu-id="3eafc-130">**Exemple de code fourni par** la [référence du programmeur Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="3eafc-130">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
