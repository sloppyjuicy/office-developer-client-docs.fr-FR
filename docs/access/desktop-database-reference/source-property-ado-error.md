---
title: Source, propriété (objet Erreur ADO)
TOCTitle: Source property (ADO Error)
ms:assetid: ffc6c77f-1494-d63a-d832-416faa4c6f07
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250316(v=office.15)
ms:contentKeyID: 48548969
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 47ae7ea790265edc10be8c907869eefbe4e593ba
ms.sourcegitcommit: 66e74e39f44dca8c41f97f05528b8f9eb1aaed87
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52061306"
---
# <a name="source-property-ado-error"></a><span data-ttu-id="71b08-102">Source, propriété (objet Erreur ADO)</span><span class="sxs-lookup"><span data-stu-id="71b08-102">Source property (ADO Error)</span></span>


<span data-ttu-id="71b08-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71b08-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71b08-104">Indique le nom de l'objet ou de l'application à l'origine d'une erreur.</span><span class="sxs-lookup"><span data-stu-id="71b08-104">Indicates the name of the object or application that originally generated an error.</span></span>

## <a name="return-value"></a><span data-ttu-id="71b08-105">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="71b08-105">Return value</span></span>

<span data-ttu-id="71b08-106">Renvoie une valeur **String** qui indique le nom d'un objet ou d'une application.</span><span class="sxs-lookup"><span data-stu-id="71b08-106">Returns a **String** value that indicates the name of an object or application.</span></span>

## <a name="remarks"></a><span data-ttu-id="71b08-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="71b08-107">Remarks</span></span>

<span data-ttu-id="71b08-108">Utilisez la propriété **Source** sur un objet [Error](error-object-ado.md) pour déterminer le nom de l'objet ou de l'application à l'origine de l'erreur.</span><span class="sxs-lookup"><span data-stu-id="71b08-108">Use the **Source** property on an [Error](error-object-ado.md) object to determine the name of the object or application that originally generated an error.</span></span> <span data-ttu-id="71b08-109">Il peut s'agir du nom de la classe ou l'ID de programme de l'objet.</span><span class="sxs-lookup"><span data-stu-id="71b08-109">This could be the object's class name or programmatic ID.</span></span> <span data-ttu-id="71b08-110">Pour les erreurs dans ADO, la valeur de la propriété est **ADODB.**</span><span class="sxs-lookup"><span data-stu-id="71b08-110">For errors in ADO, the property value will be **ADODB.**</span></span> <span data-ttu-id="71b08-111">*NomObjet*, où *NomObjet* est le nom de l’objet ayant déclenché l’erreur.</span><span class="sxs-lookup"><span data-stu-id="71b08-111">*ObjectName*, where *ObjectName* is the name of the object that triggered the error.</span></span> <span data-ttu-id="71b08-112">Pour ADOX et ADO MD, la valeur est **ADOX.**</span><span class="sxs-lookup"><span data-stu-id="71b08-112">For ADOX and ADO MD, the value will be **ADOX.**</span></span> <span data-ttu-id="71b08-113">*NomObjet* et **ADOMD.**</span><span class="sxs-lookup"><span data-stu-id="71b08-113">*ObjectName* and **ADOMD.**</span></span> <span data-ttu-id="71b08-114">*NomObjet* respectivement.</span><span class="sxs-lookup"><span data-stu-id="71b08-114">*ObjectName,* respectively.</span></span>

<span data-ttu-id="71b08-115">À partir de la documentation sur l’erreur indiquant les valeurs des propriétés **Source**, [Number](number-property-ado.md) et [Description](description-property-ado.md) des objets **Error**, vous pouvez écrire un code qui gèrera l’erreur de façon appropriée.</span><span class="sxs-lookup"><span data-stu-id="71b08-115">Based on the error documentation from the **Source**, [Number](number-property-ado.md), and [Description](description-property-ado.md) properties of **Error** objects, you can write code that will handle the error appropriately.</span></span>

<span data-ttu-id="71b08-116">La propriété **Source** des objets **Error** est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="71b08-116">The **Source** property is read-only for **Error** objects.</span></span>

