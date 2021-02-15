---
title: Flush, méthode - ActiveX Data Objects (ADO)
TOCTitle: Flush method (ADO)
ms:assetid: c167e3b1-c133-ce45-6cee-5a1280a1568f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249941(v=office.15)
ms:contentKeyID: 48547529
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a55eb66c454d510d53083c495326548eda08af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292341"
---
# <a name="flush-method-ado"></a><span data-ttu-id="81804-102">Flush, méthode (ADO)</span><span class="sxs-lookup"><span data-stu-id="81804-102">Flush method (ADO)</span></span>


<span data-ttu-id="81804-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="81804-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="81804-104">Force l’envoi de l’objet [Stream](stream-object-ado.md) conservé dans la mémoire tampon ADO vers l’objet sous-jacent auquel cet objet **Stream** est associé.</span><span class="sxs-lookup"><span data-stu-id="81804-104">Forces the contents of the [Stream](stream-object-ado.md) remaining in the ADO buffer to the underlying object with which the **Stream** is associated.</span></span>

## <a name="syntax"></a><span data-ttu-id="81804-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81804-105">Syntax</span></span>

<span data-ttu-id="81804-106">*Stream*. Flush</span><span class="sxs-lookup"><span data-stu-id="81804-106">*Stream*.Flush</span></span>

## <a name="remarks"></a><span data-ttu-id="81804-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="81804-107">Remarks</span></span>

<span data-ttu-id="81804-p101">Cette méthode peut servir à envoyer le contenu de la mémoire tampon du flux vers l'objet sous-jacent (par exemple, le nœud ou le fichier représenté par l'URL qui est la source de l'objet **Stream** ). Cette méthode doit être appelée lorsque vous souhaitez vous assurer que toutes les modifications apportées à un objet **Stream** ont été écrites. Toutefois, il n'est généralement pas nécessaire d'appeler la méthode **Flush** avec ADO, dans la mesure où ADO vide continuellement sa mémoire tampon en arrière-plan dans la mesure du possible. Les modifications apportées à un objet **Stream** sont effectuées automatiquement et ne sont pas mises en cache jusqu'à l'appel de la méthode **Flush**.</span><span class="sxs-lookup"><span data-stu-id="81804-p101">This method may be used to send the contents of the stream buffer to the underlying object (for example, the node or file represented by the URL that is the source of the **Stream** object). This method should be called when you want to ensure that all changes made to the contents of a **Stream** have been written. However, with ADO it is not usually necessary to call **Flush**, as ADO continuously flushes its buffer as much as possible in the background. Changes to the content of a **Stream** are made automatically, not cached until **Flush** is called.</span></span>

<span data-ttu-id="81804-112">La fermeture d'un objet **Stream** avec la méthode [Close](close-method-ado.md) vide automatiquement le contenu d'un objet **Stream**; il n'est pas nécessaire d'appeler explicitement la méthode **Flush** immédiatement avant l'appel de la méthode **Close**.</span><span class="sxs-lookup"><span data-stu-id="81804-112">Closing a **Stream** with the [Close](close-method-ado.md) method flushes the contents of a **Stream** automatically; there is no need to explicitly call **Flush** immediately before **Close**.</span></span>

