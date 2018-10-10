---
title: Écrire, méthode - ActiveX Data Objects (ADO)
TOCTitle: Write Method (ADO)
ms:assetid: cabe4581-409f-7f05-bd59-d495bfb2c6fd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249986(v=office.15)
ms:contentKeyID: 48547697
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 98af810c9a24d38a6b2b32db31f9a650c2d6f70a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25471842"
---
# <a name="write-method-ado"></a><span data-ttu-id="2abe2-102">Write, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="2abe2-102">Write Method (ADO)</span></span>


<span data-ttu-id="2abe2-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2abe2-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="2abe2-104">Écrit des données binaires dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2abe2-104">Writes binary data to a [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2abe2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2abe2-105">Syntax</span></span>

<span data-ttu-id="2abe2-106">*Flux de données*. Écrire la*mémoire tampon*</span><span class="sxs-lookup"><span data-stu-id="2abe2-106">*Stream*.Write*Buffer*</span></span>

## <a name="parameters"></a><span data-ttu-id="2abe2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2abe2-107">Parameters</span></span>

  - <span data-ttu-id="2abe2-108">*Buffer*</span><span class="sxs-lookup"><span data-stu-id="2abe2-108">*Buffer*</span></span>

  - <span data-ttu-id="2abe2-109">Valeur de type **Variant** contenant un tableau d'octets à écrire.</span><span class="sxs-lookup"><span data-stu-id="2abe2-109">A **Variant** that contains an array of bytes to be written.</span></span>

## <a name="remarks"></a><span data-ttu-id="2abe2-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2abe2-110">Remarks</span></span>

<span data-ttu-id="2abe2-111">Les octets spécifiés sont écrits dans l'objet **Stream** sans espaces insérés entre chaque octet.</span><span class="sxs-lookup"><span data-stu-id="2abe2-111">Specified bytes are written to the **Stream** object without any intervening spaces between each byte.</span></span>

<span data-ttu-id="2abe2-p101">La propriété [Position](position-property-ado.md) actuelle est définie par l'octet suivant les données écrites. La méthode **Write** ne tronque pas le reste des données d'un flux. Si vous souhaitez tronquer ces octets, appelez la méthode [SetEOS](seteos-method-ado.md).</span><span class="sxs-lookup"><span data-stu-id="2abe2-p101">The current [Position](position-property-ado.md) is set to the byte following the written data. The **Write** method does not truncate the rest of the data in a stream. If you want to truncate these bytes, call [SetEOS](seteos-method-ado.md).</span></span>

<span data-ttu-id="2abe2-115">Si vous écrivez après la position [EOS](eos-property-ado.md) actuelle, la valeur de la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** augmente pour contenir les nouveaux octets éventuels et **EOS** est déplacé au nouveau dernier octet de l'objet **Stream**.</span><span class="sxs-lookup"><span data-stu-id="2abe2-115">If you write past the current [EOS](eos-property-ado.md) position, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** will be increased to contain any new bytes, and **EOS** will move to the new last byte in the **Stream**.</span></span>


> [!NOTE]
> <P><span data-ttu-id="2abe2-p102">La méthode <STRONG>Write</STRONG> est utilisée avec des flux binaires (<A href="type-property-ado-stream.md">Type</A> a la valeur <STRONG>adTypeBinary</STRONG>). Pour les flux de texte (<STRONG>Type</STRONG> a la valeur <STRONG>adTypeText</STRONG>), utilisez la méthode <A href="writetext-method-ado.md">WriteText</A>.</span><span class="sxs-lookup"><span data-stu-id="2abe2-p102">The <STRONG>Write</STRONG> method is used with binary streams (<A href="type-property-ado-stream.md">Type</A> is <STRONG>adTypeBinary</STRONG>). For text streams (<STRONG>Type</STRONG> is <STRONG>adTypeText</STRONG>), use <A href="writetext-method-ado.md">WriteText</A>.</span></span></P>


