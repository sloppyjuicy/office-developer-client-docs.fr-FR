---
title: Objet Key (référence de base de données du bureau Access - ADOX)
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c77e45f52994f14d79acf424da14b55b2cdd9814
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472592"
---
# <a name="key-object-adox"></a><span data-ttu-id="33182-102">Key, objet (ADOX)</span><span class="sxs-lookup"><span data-stu-id="33182-102">Key Object (ADOX)</span></span>


<span data-ttu-id="33182-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="33182-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="33182-104">Représente un champ de clé primaire, étrangère ou unique d'une table de base de données.</span><span class="sxs-lookup"><span data-stu-id="33182-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="33182-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="33182-105">Remarks</span></span>

<span data-ttu-id="33182-106">Le code suivant permet de créer une nouvelle **clé**:</span><span class="sxs-lookup"><span data-stu-id="33182-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="33182-107">Avec les propriétés et collections d'un objet **Key**, vous pouvez :</span><span class="sxs-lookup"><span data-stu-id="33182-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="33182-108">Identifier la clé à l'aide de la propriété [Name](name-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="33182-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="33182-109">Déterminer si la clé est primaire, étrangère ou unique à l'aide de la propriété [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="33182-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="33182-110">Accéder aux colonnes de base de données de la clé à l'aide de la collection [Columns](columns-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="33182-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="33182-111">Spécifier le nom de la table connexe à l'aide de la propriété [RelatedTable](relatedtable-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="33182-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="33182-112">Déterminer l'opération effectuée lors de la suppression ou de la mise à jour d'une clé primaire à l'aide des propriétés [DeleteRule](deleterule-property-adox.md) et [UpdateRule](updaterule-property-adox.md).</span><span class="sxs-lookup"><span data-stu-id="33182-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

