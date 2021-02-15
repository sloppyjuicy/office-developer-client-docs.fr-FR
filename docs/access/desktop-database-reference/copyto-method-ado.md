---
title: CopyTo, méthode (ADO)
TOCTitle: CopyTo method (ADO)
ms:assetid: 1c1ab950-51f7-7ecc-ccd8-e689db02f06a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248958(v=office.15)
ms:contentKeyID: 48543558
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e8de2caf2abc53b0dbd014f21a85a6d54749033
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295477"
---
# <a name="copyto-method-ado"></a><span data-ttu-id="feeb6-102">CopyTo, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="feeb6-102">CopyTo method (ADO)</span></span>

<span data-ttu-id="feeb6-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="feeb6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="feeb6-104">Copie le nombre de caractères ou d’octets spécifié (selon la propriété [Type](type-property-ado-stream.md)) d’un objet [Stream](stream-object-ado.md) vers un autre objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="feeb6-104">Copies the specified number of characters or bytes (depending on [Type](type-property-ado-stream.md)) in the [Stream](stream-object-ado.md) to another **Stream** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="feeb6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="feeb6-105">Syntax</span></span>

<span data-ttu-id="feeb6-106">*Stream*. CopyTo *DestStream*, *NumChars*</span><span class="sxs-lookup"><span data-stu-id="feeb6-106">*Stream*.CopyTo *DestStream*, *NumChars*</span></span>

## <a name="parameters"></a><span data-ttu-id="feeb6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="feeb6-107">Parameters</span></span>

|<span data-ttu-id="feeb6-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="feeb6-108">Parameter</span></span>|<span data-ttu-id="feeb6-109">Description</span><span class="sxs-lookup"><span data-stu-id="feeb6-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="feeb6-110">*DestStream*</span><span class="sxs-lookup"><span data-stu-id="feeb6-110">*DestStream*</span></span> |<span data-ttu-id="feeb6-111">Valeur de variable objet qui contient une référence à un objet **Stream** ouvert.</span><span class="sxs-lookup"><span data-stu-id="feeb6-111">An object variable value that contains a reference to an open **Stream** object.</span></span> <span data-ttu-id="feeb6-112">Le **flux actuel** est copié dans le flux **de** destination spécifié par *DestStream*.</span><span class="sxs-lookup"><span data-stu-id="feeb6-112">The current **Stream** is copied to the destination **Stream** specified by *DestStream*.</span></span> <span data-ttu-id="feeb6-113">Le **flux** de destination doit déjà être ouvert.</span><span class="sxs-lookup"><span data-stu-id="feeb6-113">The destination **Stream** must already be open.</span></span> <span data-ttu-id="feeb6-114">Si ce n’est pas le cas, une erreur d’exécuter se produit.</span><span class="sxs-lookup"><span data-stu-id="feeb6-114">If not, a run-time error occurs.</span></span><br/><br/><span data-ttu-id="feeb6-115">**REMARQUE**: le *paramètre DestStream* peut ne pas être un proxy de l’objet **Stream,** car cela nécessite l’accès à une interface privée sur l’objet **Stream** qui ne peut pas être distante vers le client.</span><span class="sxs-lookup"><span data-stu-id="feeb6-115">**NOTE**: The *DestStream* parameter may not be a proxy of the **Stream** object because this requires access to a private interface on the **Stream** object that cannot be remoted to the client.</span></span>|
|<span data-ttu-id="feeb6-116">*NumChars*</span><span class="sxs-lookup"><span data-stu-id="feeb6-116">*NumChars*</span></span> |<span data-ttu-id="feeb6-p102">Facultatif. Valeur de type **Integer** qui spécifie le nombre d’octets ou de caractères à copier de la position actuelle dans l’objet **Stream** source vers l’objet **Stream** de destination. La valeur par défaut est –1, ce qui signifie que tous les caractères ou tous les octets sont copiés de la position actuelle vers [EOS](eos-property-ado.md).</span><span class="sxs-lookup"><span data-stu-id="feeb6-p102">Optional. An **Integer** value that specifies the number of bytes or characters to be copied from the current position in the source **Stream** to the destination **Stream**. The default value is –1, which specifies that all characters or bytes are copied from the current position to [EOS](eos-property-ado.md).</span></span>|

## <a name="remarks"></a><span data-ttu-id="feeb6-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="feeb6-120">Remarks</span></span>

<span data-ttu-id="feeb6-p103">Cette méthode copie le nombre spécifié de caractères ou d’octets à partir de la position actuelle spécifiée par la propriété [Position](position-property-ado.md). Si le nombre spécifié est supérieur au nombre d’octets disponibles jusqu’à **EOS**, seuls les caractères ou les octets de la position actuelle jusqu’à **EOS** sont copiés. Si *NumChars* a la valeur –1 ou est omis, tous les caractères ou octets sont copiés à partir de la position actuelle.</span><span class="sxs-lookup"><span data-stu-id="feeb6-p103">This method copies the specified number of characters or bytes, starting from the current position specified by the [Position](position-property-ado.md) property. If the specified number is more than the available number of bytes until **EOS**, then only characters or bytes from the current position to **EOS** are copied. If the value of *NumChars* is –1, or omitted, all characters or bytes starting from the current position are copied.</span></span>

<span data-ttu-id="feeb6-p104">Si le flux de destination contient déjà des caractères ou des octets, tout le contenu au-delà du point où se termine la copie est conservé et n'est pas tronqué. **Position** devient l'octet suivant immédiatement le dernier octet copié. Si vous voulez tronquer ces octets, appelez la méthode [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="feeb6-p104">If there are existing characters or bytes in the destination stream, all contents beyond the point where the copy ends remain, and are not truncated. **Position** becomes the byte immediately following the last byte copied. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="feeb6-p105">Utilisez **CopyTo** pour copier des données dans un objet **Stream** de destination du même type que l’objet **Stream** source (les paramètres de la propriété **Type** de ces deux objets doivent avoir tous deux la valeur **adTypeText** ou **adTypeBinary**). Pour des objets **Stream** de texte, vous pouvez modifier le paramètre de la propriété [Charset](charset-property-ado.md) de l’objet **Stream** de destination afin de pouvoir changer le jeu de caractères. Par ailleurs, vous pouvez copier des objets **Stream** de texte dans des objets **Stream** binaires, mais pas des objets **Stream** binaires dans des objets **Stream** de texte.</span><span class="sxs-lookup"><span data-stu-id="feeb6-p105">**CopyTo** should be used to copy data to a destination **Stream** of the same type as the source **Stream** (their **Type** property settings are both **adTypeText** or both **adTypeBinary**). For text **Stream** objects, you can change the [Charset](charset-property-ado.md) property setting of the destination **Stream** to translate from one character set to another. Also, text **Stream** objects can be successfully copied into binary **Stream** objects, but binary **Stream** objects cannot be copied into text **Stream** objects.</span></span>

