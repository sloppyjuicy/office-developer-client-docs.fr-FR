---
title: OriginalValue, propriété (ADO)
TOCTitle: OriginalValue property (ADO)
ms:assetid: 02ffc728-4692-d439-e2a6-2f02cca53a71
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248798(v=office.15)
ms:contentKeyID: 48542974
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0724320e1aaa1e7bfd3ceab8cf54afd5921c7425
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288181"
---
# <a name="originalvalue-property-ado"></a><span data-ttu-id="216b1-102">OriginalValue, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="216b1-102">OriginalValue property (ADO)</span></span>

<span data-ttu-id="216b1-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="216b1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="216b1-104">Indique la valeur d'un objet [Field](field-object-ado.md) existant dans l'enregistrement avant qu'aucune modification n'ait été apportée.</span><span class="sxs-lookup"><span data-stu-id="216b1-104">Indicates the value of a [Field](field-object-ado.md) that existed in the record before any changes were made.</span></span>

## <a name="return-value"></a><span data-ttu-id="216b1-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="216b1-105">Return value</span></span>

<span data-ttu-id="216b1-106">Renvoie une valeur **Variant** représentant la valeur d'un champ avant modification.</span><span class="sxs-lookup"><span data-stu-id="216b1-106">Returns a **Variant** value that represents the value of a field prior to any change.</span></span>

## <a name="remarks"></a><span data-ttu-id="216b1-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="216b1-107">Remarks</span></span>

<span data-ttu-id="216b1-108">Utilisez la propriété **OriginalValue** pour renvoyer la valeur d'origine d'un champ depuis l'enregistrement actuel.</span><span class="sxs-lookup"><span data-stu-id="216b1-108">Use the **OriginalValue** property to return the original field value for a field from the current record.</span></span>

<span data-ttu-id="216b1-109">En *mode de mise à jour immédiate* (dans lequel le fournisseur écrit les modifications apportées à la source de données sous-jacente après l'appel de la méthode [Update](update-method-ado.md) ), la propriété **OriginalValue** renvoie la valeur de champ qui existait avant toute modification (c'est-à-dire, étant donné que le dernier appel de la méthode **Update** ).</span><span class="sxs-lookup"><span data-stu-id="216b1-109">In *immediate update mode* (in which the provider writes changes to the underlying data source after you call the [Update](update-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **Update** method call).</span></span> <span data-ttu-id="216b1-110">C’est la même valeur que la méthode [CancelUpdate](cancelupdate-method-ado.md) utilise pour remplacer la propriété [Value](value-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="216b1-110">This is the same value that the [CancelUpdate](cancelupdate-method-ado.md) method uses to replace the [Value](value-property-ado.md) property.</span></span>

<span data-ttu-id="216b1-p102">En *mode de mise à jour par lot* (dans lequel le fournisseur met en cache plusieurs modifications et ne les inscrit dans la source de données sous-jacente que lorsque vous appelez la méthode [UpdateBatch](updatebatch-method-ado.md)), la propriété **OriginalValue** renvoie la valeur du champ avant modification (c’est-à-dire avant le dernier appel de la méthode **UpdateBatch**). C’est cette valeur que la méthode [CancelBatch](cancelbatch-method-ado.md) utilise pour remplacer la propriété **Value**. Lorsque vous utilisez cette propriété en association avec la propriété [UnderlyingValue](underlyingvalue-property-ado.md), vous pouvez résoudre les conflits générés par les mises à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="216b1-p102">In *batch update mode* (in which the provider caches multiple changes and writes them to the underlying data source only when you call the [UpdateBatch](updatebatch-method-ado.md) method), the **OriginalValue** property returns the field value that existed prior to any changes (that is, since the last **UpdateBatch** method call). This is the same value that the [CancelBatch](cancelbatch-method-ado.md) method uses to replace the **Value** property. When you use this property with the [UnderlyingValue](underlyingvalue-property-ado.md) property, you can resolve conflicts that arise from batch updates.</span></span>

## <a name="record"></a><span data-ttu-id="216b1-114">Record</span><span class="sxs-lookup"><span data-stu-id="216b1-114">Record</span></span>

<span data-ttu-id="216b1-115">Pour les objets [Record](record-object-ado.md), la propriété **OriginalValue** est vide pour les champs ajoutés avant l’appel de la méthode [Update](update-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="216b1-115">For [Record](record-object-ado.md) objects, the **OriginalValue** property will be empty for fields added before [Update](update-method-ado.md) is called.</span></span>

