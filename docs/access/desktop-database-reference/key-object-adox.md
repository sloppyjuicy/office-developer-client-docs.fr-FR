---
title: Objet Key (référence de base de données du bureau Access - ADOX)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7722130c76516eaa7dcaf0598a5e1c040e21ba25
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025944"
---
# <a name="key-object-adox"></a><span data-ttu-id="6dcbd-102">Key, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="6dcbd-102">Key object (ADOX)</span></span>


<span data-ttu-id="6dcbd-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6dcbd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6dcbd-104">Représente un champ de clé primaire, étrangère ou unique d'une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="6dcbd-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="6dcbd-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="6dcbd-105">Remarks</span></span>

<span data-ttu-id="6dcbd-106">Le code suivant permet de créer une nouvelle **clé**:</span><span class="sxs-lookup"><span data-stu-id="6dcbd-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="6dcbd-107">Avec les propriétés et collections d'un objet **Key**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="6dcbd-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="6dcbd-108">Identifier la clé à l'aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6dcbd-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="6dcbd-109">Déterminer si la clé est primaire, étrangère ou unique à l'aide de la propriété [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox).</span><span class="sxs-lookup"><span data-stu-id="6dcbd-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="6dcbd-110">Accéder aux colonnes de base de données de la clé à l'aide de la collection [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6dcbd-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="6dcbd-111">Spécifier le nom de la table connexe à l'aide de la propriété [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6dcbd-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="6dcbd-112">Déterminer l'opération effectuée lors de la suppression ou de la mise à jour d'une clé primaire à l'aide des propriétés [DeleteRule](deleterule-property-adox.md) et [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="6dcbd-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

