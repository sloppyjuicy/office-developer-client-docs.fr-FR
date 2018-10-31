---
title: StreamReadEnum (référence de base de données du bureau Access)
TOCTitle: StreamReadEnum
ms:assetid: 12432c0d-dc2e-10ea-13db-0c07b6ba29bc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248895(v=office.15)
ms:contentKeyID: 48543336
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 69a8c49fd9d07c1e0d67a91e131be76ad9803ad0
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861049"
---
# <a name="streamreadenum"></a><span data-ttu-id="43a46-102">StreamReadEnum</span><span class="sxs-lookup"><span data-stu-id="43a46-102">StreamReadEnum</span></span>

<span data-ttu-id="43a46-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="43a46-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="43a46-104">Spécifie si la chaîne de données entière ou si la ligne suivante doit être lue depuis un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="43a46-104">Specifies whether the whole stream or the next line should be read from a [Stream](stream-object-ado.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="43a46-105">Constant</span><span class="sxs-lookup"><span data-stu-id="43a46-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="43a46-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="43a46-106">Value</span></span></p></th>
<th><p><span data-ttu-id="43a46-107">Description</span><span class="sxs-lookup"><span data-stu-id="43a46-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43a46-108"><strong>adReadAll</strong></span><span class="sxs-lookup"><span data-stu-id="43a46-108"><strong>adReadAll</strong></span></span></p></td>
<td><p><span data-ttu-id="43a46-109">-1</span><span class="sxs-lookup"><span data-stu-id="43a46-109">-1</span></span></p></td>
<td><p><span data-ttu-id="43a46-p101">Par défaut. Lit tous les octets de la chaîne de données, depuis la position en cours jusqu’au marqueur <a href="eos-property-ado.md">EOS</a>. C’est la seule valeur à chaînes binaires <strong>StreamReadEnum</strong> valide (le <a href="type-property-ado-stream.md">Type</a> est <strong>adTypeBinary</strong>).</span><span class="sxs-lookup"><span data-stu-id="43a46-p101">Default. Reads all bytes from the stream, from the current position onwards to the <a href="eos-property-ado.md">EOS</a> marker. This is the only valid <strong>StreamReadEnum</strong> value with binary streams (<a href="type-property-ado-stream.md">Type</a> is <strong>adTypeBinary</strong>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43a46-113"><strong>adReadLine</strong></span><span class="sxs-lookup"><span data-stu-id="43a46-113"><strong>adReadLine</strong></span></span></p></td>
<td><p><span data-ttu-id="43a46-114">-2</span><span class="sxs-lookup"><span data-stu-id="43a46-114">-2</span></span></p></td>
<td><p><span data-ttu-id="43a46-115">Lit la ligne suivante de la chaîne (désignée par la propriété <a href="lineseparator-property-ado.md">LineSeparator</a>).</span><span class="sxs-lookup"><span data-stu-id="43a46-115">Reads the next line from the stream (designated by the <a href="lineseparator-property-ado.md">LineSeparator</a> property).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="43a46-116">Équivalent ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="43a46-116">ADO/WFC equivalent</span></span>

<span data-ttu-id="43a46-117">Ces constantes ne possèdent pas d'équivalent ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="43a46-117">These constants do not have ADO/WFC equivalents.</span></span>

