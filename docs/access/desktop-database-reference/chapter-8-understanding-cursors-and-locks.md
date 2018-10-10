---
title: Chapitre 8 : Fonctionnement des curseurs et des verrous
TOCTitle: 'Chapter 8: Understanding Cursors and Locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 99f363522874f01268f4c1a64515bf6f2cdd6336
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470047"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="ae8e0-102">Chapitre 8 : Fonctionnement des curseurs et des verrous</span><span class="sxs-lookup"><span data-stu-id="ae8e0-102">Chapter 8: Understanding Cursors and Locks</span></span>


<span data-ttu-id="ae8e0-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="ae8e0-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="ae8e0-p101">Il est important de comprendre le fonctionnement des curseurs pour sélectionner le type de curseur le plus efficace et le mieux adapté aux impératifs d'accès aux données d'une application. Une configuration du curseur inappropriée peut rendre l'accès aux données lent et laborieux.</span><span class="sxs-lookup"><span data-stu-id="ae8e0-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="ae8e0-106">De nombreuses fonctionnalités de l'objet **Recordset** ADO sont déterminées par le type et l'emplacement du curseur mais aussi par le type de verrou.</span><span class="sxs-lookup"><span data-stu-id="ae8e0-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="ae8e0-107">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae8e0-107">This chapter covers the following topics:</span></span>

  - [<span data-ttu-id="ae8e0-108">Définition d'un curseur</span><span class="sxs-lookup"><span data-stu-id="ae8e0-108">What is a Cursor?</span></span>](what-is-a-cursor.md)

  - [<span data-ttu-id="ae8e0-109">Types de curseurs</span><span class="sxs-lookup"><span data-stu-id="ae8e0-109">Types of Cursors</span></span>](types-of-cursors.md)

  - [<span data-ttu-id="ae8e0-110">Importance de l'emplacement du curseur</span><span class="sxs-lookup"><span data-stu-id="ae8e0-110">The Significance of Cursor Location</span></span>](the-significance-of-cursor-location.md)

  - [<span data-ttu-id="ae8e0-111">Service de curseur Microsoft pour OLE DB</span><span class="sxs-lookup"><span data-stu-id="ae8e0-111">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)

  - [<span data-ttu-id="ae8e0-112">Définition d'un verrou</span><span class="sxs-lookup"><span data-stu-id="ae8e0-112">What is a Lock?</span></span>](what-is-a-lock.md)

  - [<span data-ttu-id="ae8e0-113">Utilisation de CacheSize </span><span class="sxs-lookup"><span data-stu-id="ae8e0-113">Using CacheSize</span></span>](using-cachesize.md)

  - [<span data-ttu-id="ae8e0-114">Caractéristiques de curseur et de verrou</span><span class="sxs-lookup"><span data-stu-id="ae8e0-114">Cursor and Lock Characteristics</span></span>](cursor-and-lock-characteristics.md)

