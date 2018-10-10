---
title: SetEOS, méthode (ADO)
TOCTitle: SetEOS Method (ADO)
ms:assetid: d438eecf-7ab3-a07d-b6d5-8816db4aae7c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250063(v=office.15)
ms:contentKeyID: 48547933
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 456bbf7c7235d0db01b29372ee8f70c364263cb6
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469074"
---
# <a name="seteos-method-ado"></a><span data-ttu-id="3771b-102">SetEOS, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="3771b-102">SetEOS Method (ADO)</span></span>


<span data-ttu-id="3771b-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3771b-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3771b-104">Définit la position qui représente la fin du flux.</span><span class="sxs-lookup"><span data-stu-id="3771b-104">Sets the position that is the end of the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="3771b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3771b-105">Syntax</span></span>

<span data-ttu-id="3771b-106">*Flux de données*. SetEOS</span><span class="sxs-lookup"><span data-stu-id="3771b-106">*Stream*.SetEOS</span></span>

## <a name="remarks"></a><span data-ttu-id="3771b-107">Notes</span><span class="sxs-lookup"><span data-stu-id="3771b-107">Remarks</span></span>

<span data-ttu-id="3771b-p101">**SetEOS** met à jour la valeur de la propriété [EOS](eos-property-ado.md), en définissant la valeur actuelle de la propriété [Position](position-property-ado.md) comme fin du flux. Tous les octets ou caractères qui suivent cette position sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="3771b-p101">**SetEOS** updates the value of the [EOS](eos-property-ado.md) property, by making the current [Position](position-property-ado.md) the end of the stream. Any bytes or characters following the current position are truncated.</span></span>

<span data-ttu-id="3771b-110">Dans la mesure où les méthodes [Write](write-method-ado.md), [WriteText](writetext-method-ado.md) et [CopyTo](copyto-method-ado.md) ne tronquent aucune valeur supplémentaire dans les objets **Stream** existants, vous pouvez tronquer ces octets ou caractères en définissant la nouvelle position de fin de flux avec **SetEOS**.</span><span class="sxs-lookup"><span data-stu-id="3771b-110">Since [Write](write-method-ado.md), [WriteText](writetext-method-ado.md), and [CopyTo](copyto-method-ado.md) do not truncate any extra values in existing **Stream** objects, you can truncate these bytes or characters by setting the new end-of-stream position with **SetEOS**.</span></span>


> [!WARNING]
> <P><span data-ttu-id="3771b-111">Si vous attribuez à la propriété <STRONG>EOS</STRONG> une position qui précède la fin du flux, vous perdrez toutes les données situées après la nouvelle position <STRONG>EOS</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3771b-111">If you set <STRONG>EOS</STRONG> to a position before the actual end of the stream, you will lose all data after the new <STRONG>EOS</STRONG> position.</span></span></P>


