---
title: Name, propriété (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5c7021c6f97d1aaa9c82e65eab98a3259d6eb87e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288650"
---
# <a name="name-property-adox"></a><span data-ttu-id="4fd3f-102">Name, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="4fd3f-102">Name property (ADOX)</span></span>

<span data-ttu-id="4fd3f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fd3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4fd3f-104">Indique le nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="4fd3f-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="4fd3f-105">Settings and return values</span></span>

<span data-ttu-id="4fd3f-106">Définit ou renvoie une valeur de type **String**.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fd3f-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="4fd3f-107">Remarks</span></span>

<span data-ttu-id="4fd3f-108">Les noms ne doivent pas être uniques dans une collection.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="4fd3f-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-p101">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects. The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="4fd3f-111">Pour les objets en lecture/écriture (**Column**, **Group**, **Key**, **Index**, **Table** et **User**), la valeur par défaut est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="4fd3f-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>

> [!NOTE]
> - <span data-ttu-id="4fd3f-112">Pour les clés, cette propriété est en lecture seule sur les objets **Key** déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-112">For keys, this property is read-only on **Key** objects already appended to a collection.</span></span>
> - <span data-ttu-id="4fd3f-113">[!REMARQUE] Pour les tables, elle est en lecture seule sur les objets **Table** déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="4fd3f-113">For tables, this property is read-only for **Table** objects already appended to a collection.</span></span>


