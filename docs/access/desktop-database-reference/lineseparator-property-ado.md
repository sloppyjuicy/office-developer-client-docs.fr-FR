---
title: LineSeparator, propriété (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 831b6377ade43b3be04ed21add20fbd10e48ac2f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882503"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="063a4-102">LineSeparator, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="063a4-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="063a4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="063a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="063a4-104">Indique le caractère binaire à utiliser comme le séparateur de ligne dans des objets [Stream](stream-object-ado.md) textuels.</span><span class="sxs-lookup"><span data-stu-id="063a4-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="063a4-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="063a4-105">Settings and return values</span></span>

<span data-ttu-id="063a4-p101">Définit ou renvoie une valeur [LineSeparatorsEnum](lineseparatorsenum.md) qui indique le caractère séparateur de ligne utilisé dans le **Stream**. La valeur par défaut est **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="063a4-p101">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**. The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="063a4-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="063a4-108">Remarks</span></span>

<span data-ttu-id="063a4-p102">**LineSeparator** sert à interpréter les lignes à la lecture du contenu d'un **Stream** textuel. Les lignes peuvent être ignorées grâce à la méthode [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="063a4-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="063a4-p103">**LineSeparator** n’est utilisé qu’avec les objets **Stream** textuels (dont le [Type](type-property-ado-stream.md) est **adTypeText**). Cette propriété est ignorée si le **Type** est **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="063a4-p103">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**). This property is ignored if **Type** is **adTypeBinary**.</span></span>

