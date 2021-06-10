---
title: Key Object (ADOX - Référence de base de données de bureau Access)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290751"
---
# <a name="key-object-adox"></a><span data-ttu-id="86aaf-102">Objet Key (ADOX)</span><span class="sxs-lookup"><span data-stu-id="86aaf-102">Key object (ADOX)</span></span>


<span data-ttu-id="86aaf-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86aaf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86aaf-104">Représente un champ de clé primaire, étrangère ou unique d'une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="86aaf-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="86aaf-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="86aaf-105">Remarks</span></span>

<span data-ttu-id="86aaf-106">Le code suivant permet de créer une nouvelle **clé** :</span><span class="sxs-lookup"><span data-stu-id="86aaf-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="86aaf-107">Avec les propriétés et collections d'un objet **Key**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="86aaf-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="86aaf-108">Identifier la clé à l'aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="86aaf-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="86aaf-109">Déterminer si la clé est primaire, étrangère ou unique à l'aide de la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox).</span><span class="sxs-lookup"><span data-stu-id="86aaf-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="86aaf-110">Accéder aux colonnes de base de données de la clé à l'aide de la collection [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="86aaf-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="86aaf-111">Spécifier le nom de la table connexe à l'aide de la propriété [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="86aaf-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="86aaf-112">Déterminer l'opération effectuée lors de la suppression ou de la mise à jour d'une clé primaire à l'aide des propriétés [DeleteRule](deleterule-property-adox.md) et [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="86aaf-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

