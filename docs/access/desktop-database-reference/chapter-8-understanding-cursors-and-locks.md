---
title: 'Chapitre 8 : Présentation des curseurs et des verrous'
TOCTitle: 'Chapter 8: Understanding Cursors and Locks'
ms:assetid: 889356f9-53ca-3c46-6781-b37e1f065717
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249598(v=office.15)
ms:contentKeyID: 48546139
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ff5f62bfaeb182e3399eaa82865fb492853ef30
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861098"
---
# <a name="chapter-8-understanding-cursors-and-locks"></a><span data-ttu-id="7d437-102">Chapitre 8 : Présentation des curseurs et des verrous</span><span class="sxs-lookup"><span data-stu-id="7d437-102">Chapter 8: Understanding Cursors and Locks</span></span>


<span data-ttu-id="7d437-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d437-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7d437-p101">Il est important de comprendre le fonctionnement des curseurs pour sélectionner le type de curseur le plus efficace et le mieux adapté aux impératifs d'accès aux données d'une application. Une configuration du curseur inappropriée peut rendre l'accès aux données lent et laborieux.</span><span class="sxs-lookup"><span data-stu-id="7d437-p101">It is important to understand how cursors operate so you can select the best and most efficient cursor type for an application's data-access requirements. A less-than-optimal cursor configuration can make data-access operations painfully slow.</span></span>

<span data-ttu-id="7d437-106">De nombreuses fonctionnalités de l'objet **Recordset** ADO sont déterminées par le type et l'emplacement du curseur mais aussi par le type de verrou.</span><span class="sxs-lookup"><span data-stu-id="7d437-106">Many capabilities of the ADO **Recordset** object are determined by the type and location of the cursor, as well as the lock type.</span></span>

<span data-ttu-id="7d437-107">Ce chapitre présente les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="7d437-107">This chapter covers the following topics:</span></span>

- [<span data-ttu-id="7d437-108">Définition d'un curseur</span><span class="sxs-lookup"><span data-stu-id="7d437-108">What is a Cursor?</span></span>](what-is-a-cursor.md)

- [<span data-ttu-id="7d437-109">Importance de l'emplacement du curseur</span><span class="sxs-lookup"><span data-stu-id="7d437-109">The Significance of Cursor Location</span></span>](the-significance-of-cursor-location.md)

- [<span data-ttu-id="7d437-110">Service de curseur Microsoft pour OLE DB</span><span class="sxs-lookup"><span data-stu-id="7d437-110">The Microsoft Cursor Service for OLE DB</span></span>](the-microsoft-cursor-service-for-ole-db.md)

- [<span data-ttu-id="7d437-111">Utilisation de CacheSize </span><span class="sxs-lookup"><span data-stu-id="7d437-111">Using CacheSize</span></span>](using-cachesize.md)

- [<span data-ttu-id="7d437-112">Caractéristiques de curseur et de verrou</span><span class="sxs-lookup"><span data-stu-id="7d437-112">Cursor and Lock Characteristics</span></span>](cursor-and-lock-characteristics.md)

- [<span data-ttu-id="7d437-113">Types of Cursors (ADO)</span><span class="sxs-lookup"><span data-stu-id="7d437-113">Types of Cursors (ADO)</span></span>](types-of-cursors.md)

- [<span data-ttu-id="7d437-114">What is a Lock? (ADO)</span><span class="sxs-lookup"><span data-stu-id="7d437-114">What is a Lock? (ADO)</span></span>](what-is-a-lock.md)

