---
title: LineSeparator, propriété (ADO)
TOCTitle: LineSeparator property (ADO)
ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15)
ms:contentKeyID: 48546676
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4e941339ad1c8622d1c87ada848a44fa82a9ef2d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289948"
---
# <a name="lineseparator-property-ado"></a><span data-ttu-id="1668e-102">LineSeparator, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="1668e-102">LineSeparator property (ADO)</span></span>


<span data-ttu-id="1668e-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1668e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1668e-104">Indique le caractère binaire à utiliser comme le séparateur de ligne dans des objets [Stream](stream-object-ado.md) textuels.</span><span class="sxs-lookup"><span data-stu-id="1668e-104">Indicates the binary character to be used as the line separator in text [Stream](stream-object-ado.md) objects.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="1668e-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="1668e-105">Settings and return values</span></span>

<span data-ttu-id="1668e-106">Définit ou renvoie une valeur [LineSeparatorsEnum](lineseparatorsenum.md) qui indique le caractère séparateur de ligne utilisé dans le **Stream**.</span><span class="sxs-lookup"><span data-stu-id="1668e-106">Sets or returns a [LineSeparatorsEnum](lineseparatorsenum.md) value that indicates the line separator character used in the **Stream**.</span></span> <span data-ttu-id="1668e-107">La valeur par défaut est **adCRLF**.</span><span class="sxs-lookup"><span data-stu-id="1668e-107">The default value is **adCRLF**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1668e-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="1668e-108">Remarks</span></span>

<span data-ttu-id="1668e-p102">**LineSeparator** sert à interpréter les lignes à la lecture du contenu d’un **Stream** textuel. Les lignes peuvent être ignorées grâce à la méthode [SkipLine](skipline-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="1668e-p102">**LineSeparator** is used to interpret lines when reading the content of a text **Stream**. Lines can be skipped with the [SkipLine](skipline-method-ado.md) method.</span></span>

<span data-ttu-id="1668e-111">**LineSeparator** n’est utilisé qu’avec les objets **Stream** textuels (dont le [Type](type-property-ado-stream.md) est **adTypeText**).</span><span class="sxs-lookup"><span data-stu-id="1668e-111">**LineSeparator** is used only with text **Stream** objects ([Type](type-property-ado-stream.md) is **adTypeText**).</span></span> <span data-ttu-id="1668e-112">Cette propriété est ignorée si le **Type** est **adTypeBinary**.</span><span class="sxs-lookup"><span data-stu-id="1668e-112">This property is ignored if **Type** is **adTypeBinary**.</span></span>

