---
title: Name, propriété (ADOX)
TOCTitle: Name Property (ADOX)
ms:assetid: c92a3b2b-6e3f-1ed9-c7be-bf348a0737af
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249979(v=office.15)
ms:contentKeyID: 48547674
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4ea92fcca60d0c2877bf89359aac4532356a9874
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604049"
---
# <a name="name-property-adox"></a><span data-ttu-id="2cf25-102">Name, propriété (ADOX)</span><span class="sxs-lookup"><span data-stu-id="2cf25-102">Name Property (ADOX)</span></span>


<span data-ttu-id="2cf25-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2cf25-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2cf25-104">Indique le nom de l'objet.</span><span class="sxs-lookup"><span data-stu-id="2cf25-104">Indicates the name of the object.</span></span>

<span data-ttu-id="2cf25-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="2cf25-105"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="2cf25-106">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2cf25-106">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="2cf25-107">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="2cf25-107">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="2cf25-108">master</span><span class="sxs-lookup"><span data-stu-id="2cf25-108">master</span></span>

<span data-ttu-id="2cf25-109">Définit ou renvoie une valeur de type **String**.</span><span class="sxs-lookup"><span data-stu-id="2cf25-109">Sets or returns a **String** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cf25-110">Notes</span><span class="sxs-lookup"><span data-stu-id="2cf25-110">Remarks</span></span>

<span data-ttu-id="2cf25-111">Les noms ne doivent pas être uniques dans une collection.</span><span class="sxs-lookup"><span data-stu-id="2cf25-111">Names do not have to be unique within a collection.</span></span>

<span data-ttu-id="2cf25-112">La propriété **Name** est en lecture/écriture dans la [colonne](column-object-adox.md), [groupe](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md)et les objets [utilisateur](user-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="2cf25-112">The **Name** property is read/write on [Column](column-object-adox.md), [Group](group-object-adox.md), [Key](key-object-adox.md), [Index](index-object-adox.md), [Table](table-object-adox.md), and [User](user-object-adox.md) objects.</span></span> <span data-ttu-id="2cf25-113">La propriété **Name** est en lecture seule sur les objets de [catalogue](catalog-object-adox.md), [Procedure](procedure-object-adox.md)et [View](view-object-adox.md) .</span><span class="sxs-lookup"><span data-stu-id="2cf25-113">The **Name** property is read-only on [Catalog](catalog-object-adox.md), [Procedure](procedure-object-adox.md), and [View](view-object-adox.md) objects.</span></span>

<span data-ttu-id="2cf25-114">Pour les objets en lecture/écriture (**Column**, **Group**, **Key**, **Index**, **Table** et **User**), la valeur par défaut est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="2cf25-114">For read/write objects (**Column**, **Group**, **Key**, **Index**, **Table** and **User** objects), the default value is an empty string ("").</span></span>


> [!NOTE]
> <P><span data-ttu-id="2cf25-115">[!REMARQUE] Pour les clés, cette propriété est en lecture seule sur les objets <STRONG>Key</STRONG> déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="2cf25-115">For keys, this property is read-only on <STRONG>Key</STRONG> objects already appended to a collection.</span></span></P>




> [!NOTE]
> <P><span data-ttu-id="2cf25-116">[!REMARQUE] Pour les tables, elle est en lecture seule sur les objets <STRONG>Table</STRONG> déjà ajoutés à une collection.</span><span class="sxs-lookup"><span data-stu-id="2cf25-116">For tables, this property is read-only for <STRONG>Table</STRONG> objects already appended to a collection.</span></span></P>


