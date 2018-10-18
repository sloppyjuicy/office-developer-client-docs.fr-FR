---
title: Source, propriété (objet Erreur ADO)
TOCTitle: Source Property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: adeadcf4c467aabad7b486bd43c12e26d67ce302
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603863"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="53da3-102">Source, propriété (objet Erreur ADO)</span><span class="sxs-lookup"><span data-stu-id="53da3-102">Source Property (ADO Error)</span></span>


<span data-ttu-id="53da3-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="53da3-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="53da3-104">Indique le nom de l'objet ou de l'application à l'origine d'une erreur.</span><span class="sxs-lookup"><span data-stu-id="53da3-104">Indicates the name of the object or application that originally generated an error.</span></span>

<span data-ttu-id="53da3-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="53da3-105"><<<<<<< HEAD</span></span>
## <a name="return-value"></a><span data-ttu-id="53da3-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53da3-106">Return Value</span></span>
=======
## <a name="return-value"></a><span data-ttu-id="53da3-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="53da3-107">Return value</span></span>
>>>>>>> <span data-ttu-id="53da3-108">master</span><span class="sxs-lookup"><span data-stu-id="53da3-108">master</span></span>

<span data-ttu-id="53da3-109">Renvoie une valeur **String** qui indique le nom d'un objet ou d'une application.</span><span class="sxs-lookup"><span data-stu-id="53da3-109">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="53da3-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="53da3-110">Remarks</span></span>

<span data-ttu-id="53da3-111">Utilisez la propriété **Source** sur un objet [Error](error-object-ado.md) pour déterminer le nom de l'objet ou de l'application à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="53da3-111">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="53da3-112">Il peut s'agir du nom de la classe ou l'ID de programme de l'objet.</span><span class="sxs-lookup"><span data-stu-id="53da3-112">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="53da3-113">Des erreurs dans ADO, la valeur de la propriété sera \**ADODB. \*\*\* ObjectName*, où *NomObjet* est le nom de l’objet qui a déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="53da3-113">For errors in ADO, the property value will be \**ADODB.\*\*\*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="53da3-114">Pour ADOX et ADO MD, la valeur sera \**ADOX. \*\*\* ObjectName* et \**ADOMD. \*\*\* ObjectName,* respectivement.</span><span class="sxs-lookup"><span data-stu-id="53da3-114">For ADOX and ADO MD, the value will be \**ADOX.\*\*\*ObjectName* and \**ADOMD.\*\*\*ObjectName,* respectively.</span></span>

<span data-ttu-id="53da3-115">À partir de la documentation sur l'erreur indiquant les valeurs des propriétés **Source**, [Number](number-property-ado.md) et [Description](description-property-ado.md) des objets **Error**, vous pouvez écrire un code qui gèrera l'erreur de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="53da3-115">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="53da3-116">La propriété **Source** des objets **Error** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="53da3-116">The **Source** property is read-only for **Error** objects.</span></span>

