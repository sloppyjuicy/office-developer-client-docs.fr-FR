---
title: CopyTo, méthode (ADO)
TOCTitle: CopyTo Method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2a5e5b793940c82e6656ec836c5a8d392800940d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25870141"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="00b6f-102">CopyTo, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="00b6f-102">CopyTo Method (ADO)</span></span>


<span data-ttu-id="00b6f-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="00b6f-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="00b6f-104">Copie le nombre de caractères ou d'octets spécifié (selon la propriété [Type](type-property-ado-stream.md)) d'un objet [Stream](stream-object-ado.md) vers un autre objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="00b6f-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="00b6f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00b6f-105">Syntax</span></span>

<span data-ttu-id="00b6f-106">*Flux de données*. De CopyTo *DestStream*, groupes de *NumChars*</span><span class="sxs-lookup"><span data-stu-id="00b6f-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="00b6f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="00b6f-107">Parameters</span></span>

  - <span data-ttu-id="00b6f-108">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="00b6f-108">*DestStream*</span></span>

  - <span data-ttu-id="00b6f-p101">Valeur de variable objet contenant une référence à un objet **Stream** ouvert. L'objet **Stream** actif est copié dans l'objet **Stream** de destination spécifié par *DestStream*. L'objet **Stream** de destination doit être déjà ouvert sans quoi une erreur d'exécution est générée.

</span><span class="sxs-lookup"><span data-stu-id="00b6f-p101">An object variable value that contains a reference to an open **Stream** object. The current **Stream** is copied to the destination **Stream** specified by *DestStream*. The destination **Stream** must already be open. If not, a run-time error occurs.</span></span>   

    > [!NOTE]
    > <span data-ttu-id="00b6f-113">Le paramètre *DestStream* ne peut pas être un proxy de l’objet **Stream** parce que ceci exige l’accès à une interface privée sur l’objet **Stream** qui ne peuvent pas être transférée vers le client.</span><span class="sxs-lookup"><span data-stu-id="00b6f-113">The *DestStream* parameter may not be a proxy of the **Stream** object because this requires access to a private interface on the **Stream** object that cannot be remoted to the client.</span></span>

  - <span data-ttu-id="00b6f-114">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="00b6f-114">*NumChars*</span></span>

  - <span data-ttu-id="00b6f-115">Facultatif.</span><span class="sxs-lookup"><span data-stu-id="00b6f-115">Optional.</span></span> <span data-ttu-id="00b6f-116">Valeur de type **Integer** qui spécifie le nombre d'octets ou de caractères à copier de la position actuelle dans l'objet **Stream** source vers l'objet **Stream** de destination.</span><span class="sxs-lookup"><span data-stu-id="00b6f-116">An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**.</span></span> <span data-ttu-id="00b6f-117">La valeur par défaut est – 1, ce qui spécifie que tous les caractères ou octets sont copiés à partir de la position actuelle vers [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="00b6f-117">The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00b6f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="00b6f-118">Remarks</span></span>

<span data-ttu-id="00b6f-119">Cette méthode copie le nombre spécifié de caractères ou d'octets à partir de la position actuelle spécifiée par la propriété [Position](position-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="00b6f-119">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property.</span></span> <span data-ttu-id="00b6f-120">Si le nombre spécifié est supérieur au nombre d'octets disponibles jusqu'à **EOS**, seuls les caractères ou les octets de la position actuelle jusqu'à **EOS** sont copiés.</span><span class="sxs-lookup"><span data-stu-id="00b6f-120">If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied.</span></span> <span data-ttu-id="00b6f-121">Si la valeur de *NumChars* est – 1 ou est omis, tous les caractères ou octets à partir de la position actuelle sont copiés.</span><span class="sxs-lookup"><span data-stu-id="00b6f-121">If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="00b6f-p104">Si le flux de destination contient déjà des caractères ou des octets, tout le contenu au-delà du point où se termine la copie est conservé et n'est pas tronqué. **Position** devient l'octet suivant immédiatement le dernier octet copié. Si vous voulez tronquer ces octets, appelez la méthode [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="00b6f-p104">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated. **Position** becomes the byte immediately following the last byte copied. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="00b6f-p105">Utilisez **CopyTo** pour copier des données dans un objet **Stream** de destination du même type que l’objet **Stream** source (les paramètres de la propriété **Type** de ces deux objets doivent avoir tous deux la valeur **adTypeText** ou **adTypeBinary**). Pour des objets **Stream** de texte, vous pouvez modifier le paramètre de la propriété [Charset](charset-property-ado.md) de l’objet **Stream** de destination afin de pouvoir changer le jeu de caractères. Par ailleurs, vous pouvez copier des objets **Stream** de texte dans des objets **Stream** binaires, mais pas des objets **Stream** binaires dans des objets **Stream** de texte.</span><span class="sxs-lookup"><span data-stu-id="00b6f-p105">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**). For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another. Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

