---
title: Position, propriété (ADO)
TOCTitle: Position property (ADO)
ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15)
ms:contentKeyID: 48546709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 6a47cc394cf0bb1c6f5a3d707c1885d0abef0f0e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704230"
---
# <a name="position-property-ado"></a><span data-ttu-id="57c48-102">Position, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="57c48-102">Position property (ADO)</span></span>

<span data-ttu-id="57c48-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="57c48-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="57c48-104">Indique la position actuelle dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="57c48-104">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="57c48-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="57c48-105">Settings and return values</span></span>

<span data-ttu-id="57c48-p101">Définit ou retourne une valeur de type **Long** qui spécifie le décalage, en nombre d'octets, de la position actuelle par rapport au début du flux. La valeur par défaut est 0 ; elle représente le premier octet du flux.</span><span class="sxs-lookup"><span data-stu-id="57c48-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="57c48-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="57c48-108">Remarks</span></span>

<span data-ttu-id="57c48-p102">La position actuelle peut être définie au-delà de la fin du flux. Dans ce cas, la propriété [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) de l'objet **Stream** est augmentée en conséquence. Les nouveaux octets ajoutés de cette façon sont nuls.</span><span class="sxs-lookup"><span data-stu-id="57c48-p102">The current position can be moved to a point after the end of the stream. If you specify the current position beyond the end of the stream, the [Size](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream) of the **Stream** object will be increased accordingly. Any new bytes added in this way will be null.</span></span>

> [!NOTE]
> <span data-ttu-id="57c48-p103">[!REMARQUE] **Position** mesure toujours des octets. Pour les flux de texte utilisant des jeux de caractères multioctet, multipliez la position par la taille de caractères pour déterminer le numéro du caractère. Par exemple, dans un jeu de caractères de deux octets, le premier caractère est en position 0, le deuxième en position 2, le troisième en position 4, etc.</span><span class="sxs-lookup"><span data-stu-id="57c48-p103">**Position** always measures bytes. For text streams using multibyte character sets, multiply the position by the character size to determine the character number. For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span>

<span data-ttu-id="57c48-p104">Il est impossible d'utiliser des valeurs négatives pour modifier la position actuelle dans un **Stream**. La propriété **Position** n'accepte que les chiffres positifs.</span><span class="sxs-lookup"><span data-stu-id="57c48-p104">Negative values cannot be used to change the current position in a **Stream**. Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="57c48-117">Pour les objets **Stream** en lecture seule, ADO ne renvoie pas une erreur si la **Position** est définie sur une valeur supérieure à la **taille** du **flux de données**.</span><span class="sxs-lookup"><span data-stu-id="57c48-117">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**.</span></span> <span data-ttu-id="57c48-118">Cela ne pas modifier la taille du **flux**ou **son contenu** .</span><span class="sxs-lookup"><span data-stu-id="57c48-118">This does not change the size of the **Stream**, or alter the **Stream** contents in any way.</span></span> <span data-ttu-id="57c48-119">Toutefois, cette opération doit être évitée, car elle génère une valeur de **Position** sans signification.</span><span class="sxs-lookup"><span data-stu-id="57c48-119">However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

