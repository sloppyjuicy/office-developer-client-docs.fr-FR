---
title: 'Chapitre 8 : Présentation des curseurs et des verrous'
TOCTitle: 'Chapter 8: Understanding cursors and locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3075c0c9bd8267f6b30773a846523172eb2ef603
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726091"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="21324-102">Chapitre 8 : Présentation des curseurs et des verrous</span><span class="sxs-lookup"><span data-stu-id="21324-102">Chapter 8: Understanding cursors and locks</span></span>

<span data-ttu-id="21324-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="21324-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="21324-p101">Il est important de comprendre le fonctionnement des curseurs pour sélectionner le type de curseur le plus efficace et le mieux adapté aux impératifs d'accès aux données d'une application. Une configuration du curseur inappropriée peut rendre l'accès aux données lent et laborieux.</span><span class="sxs-lookup"><span data-stu-id="21324-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="21324-106">De nombreuses fonctionnalités de l'objet **Recordset** ADO sont déterminées par le type et l'emplacement du curseur mais aussi par le type de verrou.</span><span class="sxs-lookup"><span data-stu-id="21324-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="21324-107">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="21324-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="21324-108">Qu’est un curseur ?</span><span class="sxs-lookup"><span data-stu-id="21324-108">What is a cursor?</span></span>](what-is-a-cursor.md)
- [<span data-ttu-id="21324-109">L’importance de l’emplacement du curseur</span><span class="sxs-lookup"><span data-stu-id="21324-109">The significance of cursor location</span></span>](the-significance-of-cursor-location.md)
- [<span data-ttu-id="21324-110">Service de curseur Microsoft pour OLE DB</span><span class="sxs-lookup"><span data-stu-id="21324-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)
- [<span data-ttu-id="21324-111">Utilisation de CacheSize </span><span class="sxs-lookup"><span data-stu-id="21324-111">Using CacheSize</span></span>](using-cachesize.md)
- [<span data-ttu-id="21324-112">Caractéristiques de curseur et de verrou</span><span class="sxs-lookup"><span data-stu-id="21324-112">Cursor and lock characteristics</span></span>](cursor-and-lock-characteristics.md)
- [<span data-ttu-id="21324-113">Types de curseurs (ADO)</span><span class="sxs-lookup"><span data-stu-id="21324-113">Types of cursors (ADO)</span></span>](types-of-cursors.md)
- [<span data-ttu-id="21324-114">Qu’est un verrou ? (ADO)</span><span class="sxs-lookup"><span data-stu-id="21324-114">What is a lock? (ADO)</span></span>](what-is-a-lock.md)

