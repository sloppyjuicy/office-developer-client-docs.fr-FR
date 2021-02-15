---
title: Property, objet (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e26bc59221b4ff55c943b6a9a0c87ac5c0dd936b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301189"
---
# <a name="property-object-dao"></a><span data-ttu-id="2c64f-102">Property, objet (DAO)</span><span class="sxs-lookup"><span data-stu-id="2c64f-102">Property object (DAO)</span></span>

<span data-ttu-id="2c64f-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c64f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c64f-104">Un objet **Property** représente une caractéristique prédéfinie ou définie par l'utilisateur d'un objet DAO.</span><span class="sxs-lookup"><span data-stu-id="2c64f-104">A **Property** object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c64f-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="2c64f-105">Remarks</span></span>

<span data-ttu-id="2c64f-p101">À l'exception des objets **Connection** et **Error**, chaque objet DAO intègre une collection **Properties** qui contient des objets **Property** correspondant à des propriétés prédéfinies de cet objet DAO. L'utilisateur peut également définir des objets **Property** et les ajouter à la collection **Properties** de certains objets DAO. Ces objets **Property** (qui sont souvent appelés propriétés) caractérisent de façon unique cette instance de l'objet.</span><span class="sxs-lookup"><span data-stu-id="2c64f-p101">Every DAO object except the **Connection** and **Error** objects contains a **Properties** collection which has **Property** objects corresponding to built-in properties of that DAO object. The user can also define **Property** objects and append them to the **Properties** collection of some DAO objects. These **Property** objects (which are often just called properties) uniquely characterize that instance of the object.</span></span>

<span data-ttu-id="2c64f-109">Vous pouvez créer des propriétés définies par l'utilisateur pour les objets suivants :</span><span class="sxs-lookup"><span data-stu-id="2c64f-109">You can create user-defined properties for the following objects:</span></span>

- <span data-ttu-id="2c64f-110">objets **Database**, **Index**, **QueryDef** et **TableDef**;</span><span class="sxs-lookup"><span data-stu-id="2c64f-110">**Database**, **Index**, **QueryDef**, and **TableDef** objects</span></span>

- <span data-ttu-id="2c64f-111">objets **Field** dans les collections **Fields** d'objets **QueryDef** et **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="2c64f-111">**Field** objects in **Fields** collections of **QueryDef** and **TableDef** objects</span></span>

<span data-ttu-id="2c64f-p102">Pour ajouter une propriété définie par l'utilisateur, utilisez la méthode **CreateProperty** pour créer un objet **Property** en fonction d'un paramètre de propriété **Name** unique. Définissez les propriétés **Type** et **Value** du nouvel objet **Property**, puis ajoutez-le à la collection **Properties** de l'objet approprié. L'objet auquel vous ajoutez la propriété définie par l'utilisateur doit déjà avoir été ajouté à une collection. La référence d'un objet **Property** défini par l'utilisateur qui n'a pas encore été ajouté à une collection **Properties** entraîne une erreur, de même que l'ajout d'un objet **Property** défini par l'utilisateur à une collection **Properties** contenant un objet **Property** du même nom.</span><span class="sxs-lookup"><span data-stu-id="2c64f-p102">To add a user-defined property, use the **CreateProperty** method to create a **Property** object with a unique **Name** property setting. Set the **Type** and **Value** properties of the new **Property** object, and then append it to the **Properties** collection of the appropriate object. The object to which you are adding the user-defined property must already be appended to a collection. Referencing a user-defined **Property** object that has not yet been appended to a **Properties** collection will cause an error, as will appending a user-defined **Property** object to a **Properties** collection containing a **Property** object of the same name.</span></span>

<span data-ttu-id="2c64f-116">Vous pouvez supprimer les propriétés définies par l'utilisateur de la collection **Properties**, mais vous ne pouvez pas supprimer les propriétés prédéfinies.</span><span class="sxs-lookup"><span data-stu-id="2c64f-116">You can delete user-defined properties from the **Properties** collection, but you can't delete built-in properties.</span></span>

> [!NOTE]
> <span data-ttu-id="2c64f-p103">[!REMARQUE] Un objet **Property** défini par l'utilisateur est associé uniquement à l'instance spécifique d'un objet. La propriété n'est pas définie pour toutes les instances d'objets du type sélectionné.</span><span class="sxs-lookup"><span data-stu-id="2c64f-p103">A user-defined **Property** object is associated only with the specific instance of an object. The property isn't defined for all instances of objects of the selected type.</span></span>

<span data-ttu-id="2c64f-119">Vous pouvez utiliser la collection **Properties** d'un objet pour énumérer les propriétés prédéfinies et définies par l'utilisateur de l'objet.</span><span class="sxs-lookup"><span data-stu-id="2c64f-119">You can use the **Properties** collection of an object to enumerate the object's built-in and user-defined properties.</span></span> <span data-ttu-id="2c64f-120">Vous ne devez pas connaître au préalable les propriétés exactes existantes ou leurs caractéristiques (propriétés **Name** et **Type**) pour les manipuler.</span><span class="sxs-lookup"><span data-stu-id="2c64f-120">You don't need to know beforehand exactly which properties exist or what their characteristics (**Name** and **Type** properties) are to manipulate them.</span></span> <span data-ttu-id="2c64f-121">Toutefois, une erreur se produit lorsque vous tentez de lire une propriété en écriture seule (propriété **Password** d'un objet **Workspace**, par exemple) ou de lire ou d'écrire une propriété dans un contexte inapproprié, comme le paramètre de propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="2c64f-121">However, if you try to read a write-only property, such as the **Password** property of a **Workspace** object, or try to read or write a property in an inappropriate context, such as the **Value** property setting of a **Field** object in the **Fields** collection of a **TableDef** object, an error occurs.</span></span>

<span data-ttu-id="2c64f-122">En outre, l'objet **Property** intègre quatre propriétés prédéfinies :</span><span class="sxs-lookup"><span data-stu-id="2c64f-122">The **Property** object also has four built-in properties:</span></span>

- <span data-ttu-id="2c64f-123">la propriété **Name**, une valeur de type **String** qui identifie de façon unique la propriété ;</span><span class="sxs-lookup"><span data-stu-id="2c64f-123">The **Name** property, a **String** that uniquely identifies the property.</span></span>

- <span data-ttu-id="2c64f-124">la propriété **Type**, une valeur de type **Integer** qui spécifie le type de données de la propriété ;</span><span class="sxs-lookup"><span data-stu-id="2c64f-124">The **Type** property, an **Integer** that specifies the property data type.</span></span>

- <span data-ttu-id="2c64f-125">la propriété **Value**, une valeur de type **Variant** qui contient la valeur de propriété ;</span><span class="sxs-lookup"><span data-stu-id="2c64f-125">The **Value** property, a **Variant** that contains the property setting.</span></span>

- <span data-ttu-id="2c64f-p105">la propriété **Inherited**, une valeur de type **Boolean** qui indique si la propriété est héritée d'un autre objet. Par exemple, un objet **Field** dans une collection **Fields** d'un objet **Recordset** peut hériter des propriétés issues de l'objet **TableDef** ou **QueryDef** sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="2c64f-p105">The **Inherited** property, a **Boolean** that indicates whether the property is inherited from another object. For example, a **Field** object in a **Fields** collection of a **Recordset** object can inherit properties from the underlying **TableDef** or **QueryDef** object.</span></span>

<span data-ttu-id="2c64f-128">Pour faire référence à un objet **Property** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :</span><span class="sxs-lookup"><span data-stu-id="2c64f-128">To refer to a built-in **Property** object in a collection by its ordinal number or by its **Name** property setting, use any of the following syntax forms:</span></span>

- <span data-ttu-id="2c64f-129">\*object\***. Propriétés**(0)</span><span class="sxs-lookup"><span data-stu-id="2c64f-129">\*object\***.Properties**(0)</span></span>

- <span data-ttu-id="2c64f-130">*object\***. Propriétés**( »* name\* »)</span><span class="sxs-lookup"><span data-stu-id="2c64f-130">*object\***.Properties**("* name\*")</span></span>

- <span data-ttu-id="2c64f-131">*object\*\*\*. Nom des*\* \! \[\* propriétés\*\]</span><span class="sxs-lookup"><span data-stu-id="2c64f-131">*object\***.Properties**\!\[* name\*\]</span></span>

<span data-ttu-id="2c64f-132">Dans le cas d'une propriété prédéfinie, vous pouvez également utiliser la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="2c64f-132">For a built-in property, you can also use this syntax:</span></span>

- <span data-ttu-id="2c64f-133">*.* *name*</span><span class="sxs-lookup"><span data-stu-id="2c64f-133">*object*.*name*</span></span>

> [!NOTE]
> <span data-ttu-id="2c64f-134">Pour une propriété définie par l’utilisateur, vous devez utiliser l’objet *complet\*\*\*. Syntaxe des*\* propriétés*(« nom* »).</span><span class="sxs-lookup"><span data-stu-id="2c64f-134">For a user-defined property, you must use the full *object\***.Properties**("* name\*") syntax.</span></span>

<span data-ttu-id="2c64f-p106">Avec les mêmes formes de syntaxe, vous pouvez également faire référence à la propriété **Value** d'un objet **Property**. C'est le contexte de la référence qui indique si vous faites référence à l'objet **Property** ou à la propriété **Value** de l'objet **Property**.</span><span class="sxs-lookup"><span data-stu-id="2c64f-p106">With the same syntax forms, you can also refer to the **Value** property of a **Property** object. The context of the reference will determine whether you are referring to the **Property** object itself or the **Value** property of the **Property** object.</span></span>

