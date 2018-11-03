---
title: Name, propriété (ADOX)
TOCTitle: Name property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a65bad49c7b9b7a7af91403b1119923b62daa04a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25931245"
---
# <a name="name-property-adox"></a><span data-ttu-id="82f42-102">Name, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="82f42-102">Name property (ADOX)</span></span>


<span data-ttu-id="82f42-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="82f42-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="82f42-104">Indique le nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="82f42-104">Indicates the name of the object.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="82f42-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="82f42-105">Settings and return values</span></span>

<span data-ttu-id="82f42-106">Définit ou renvoie une valeur de type **String**.</span><span class="sxs-lookup"><span data-stu-id="82f42-106">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="82f42-107">Notes</span><span class="sxs-lookup"><span data-stu-id="82f42-107">Remarks</span></span>

<span data-ttu-id="82f42-108">Les noms ne doivent pas être uniques dans une collection.</span><span class="sxs-lookup"><span data-stu-id="82f42-108">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="82f42-109">La propriété **Name** est en lecture/écriture dans la [colonne](column-object-adox.md), [groupe](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md)et les objets [utilisateur](user-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="82f42-109">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects.</span></span> <span data-ttu-id="82f42-110">La propriété **Name** est en lecture seule sur les objets de [catalogue](catalog-object-adox.md), [Procedure](procedure-object-adox.md)et [View](view-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="82f42-110">The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="82f42-111">Pour les objets en lecture/écriture (**Column**, **Group**, **Key**, **Index**, **Table** et **User**), la valeur par défaut est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="82f42-111">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="82f42-112">[!REMARQUE] Pour les clés, cette propriété est en lecture seule sur les objets <STRONG>Key</STRONG> déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="82f42-112">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="82f42-113">[!REMARQUE] Pour les tables, elle est en lecture seule sur les objets <STRONG>Table</STRONG> déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="82f42-113">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


