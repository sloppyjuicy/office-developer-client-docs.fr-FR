---
title: Read, méthode - ActiveX Data Objects (ADO)
TOCTitle: Read Method (ADO)
ms:assetid: 91c3ad34-f891-5be0-1fc1-c5c8a2ff07a4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249641(v=office.15)
ms:contentKeyID: 48546357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b47b557fcb3e3c9ed26af29ce910c95262e4fe13
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884946"
---
# <a name="read-method-ado"></a><span data-ttu-id="7ad24-102">Read, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="7ad24-102">Read Method (ADO)</span></span>


<span data-ttu-id="7ad24-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ad24-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ad24-104">Lit un nombre spécifié d'octets dans un objet [Stream](stream-object-ado.md) binaire.</span><span class="sxs-lookup"><span data-stu-id="7ad24-104">Reads a specified number of bytes from a binary [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ad24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7ad24-105">Syntax</span></span>

<span data-ttu-id="7ad24-106">*Variant* = *flux*. Lecture (*NbOctets* )</span><span class="sxs-lookup"><span data-stu-id="7ad24-106">*Variant* = *Stream*.Read (*NumBytes* )</span></span>

## <a name="parameters"></a><span data-ttu-id="7ad24-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7ad24-107">Parameters</span></span>

  - <span data-ttu-id="7ad24-108">*Valeur du paramètre NbOctets*</span><span class="sxs-lookup"><span data-stu-id="7ad24-108">*NumBytes*</span></span>

  - <span data-ttu-id="7ad24-p101">Facultatif. Valeur de type **Long** qui spécifie le nombre d'octets à lire dans le fichier ou la valeur [StreamReadEnum ](streamreadenum.md) **adReadAll**, qui constitue la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7ad24-p101">Optional. A **Long** value that specifies the number of bytes to read from the file or the [StreamReadEnum](streamreadenum.md) value **adReadAll**, which is the default.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ad24-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7ad24-111">Return value</span></span>

<span data-ttu-id="7ad24-112">La méthode **Read** lit un nombre spécifié d'octets ou l'intégralité du flux d'un objet **Stream** et retourne les données résultantes sous la forme de données de type **Variant**.</span><span class="sxs-lookup"><span data-stu-id="7ad24-112">The **Read** method reads a specified number of bytes or the entire stream from a **Stream** object and returns the resulting data as a **Variant**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ad24-113">Notes</span><span class="sxs-lookup"><span data-stu-id="7ad24-113">Remarks</span></span>

<span data-ttu-id="7ad24-p102">Si la valeur de *NbOctets* est supérieure au nombre d'octets laissés dans l'objet **Stream**, seuls les octets restants sont retournés. Les données lues ne sont pas remplies afin de correspondre à la longueur spécifiée par *NbOctets*. S'il ne reste plus d'octet à lire, une valeur de type Variant NULL est retournée. La méthode **Read** ne peut pas être utilisée pour lire à l'envers.</span><span class="sxs-lookup"><span data-stu-id="7ad24-p102">If *NumBytes* is more than the number of bytes left in the **Stream**, only the bytes remaining are returned. The data read is not padded to match the length specified by *NumBytes*. If there are no bytes left to read, a variant with a null value is returned. **Read** cannot be used to read backwards.</span></span>


> [!NOTE]
> <P><span data-ttu-id="7ad24-p103"><EM>NbOctets</EM> mesure toujours des octets. Pour les objets <STRONG>Stream</STRONG> contenant du texte (<A href="type-property-ado-stream.md">Type </A><STRONG>adTypeText</STRONG>), utilisez <A href="readtext-method-ado.md">ReadText</A>.</span><span class="sxs-lookup"><span data-stu-id="7ad24-p103"><EM>NumBytes</EM> always measures bytes. For text <STRONG>Stream</STRONG> objects (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeText</STRONG>), use <A href="readtext-method-ado.md">ReadText</A>.</span></span></P>


