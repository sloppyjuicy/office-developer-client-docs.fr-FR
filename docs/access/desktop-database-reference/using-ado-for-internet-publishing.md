---
title: Utilisation d'ADO pour la publication Internet
TOCTitle: Using ADO for Internet Publishing
ms:assetid: 1e829783-fc12-e303-6f12-2df1ca96cb0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248975(v=office.15)
ms:contentKeyID: 48543622
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae8341151c7bf7d90585794061647ba33a5c4ea7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32305900"
---
# <a name="using-ado-for-internet-publishing"></a><span data-ttu-id="4ac67-102">Utilisation d’ADO pour la publication Internet</span><span class="sxs-lookup"><span data-stu-id="4ac67-102">Using ADO for Internet publishing</span></span>


<span data-ttu-id="4ac67-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4ac67-103">**Applies to**: Access 2013, Office 2013</span></span>



<span data-ttu-id="4ac67-104">Le [fournisseur OLE DB pour la publication Internet](the-ole-db-provider-for-internet-publishing.md) montre un exemple spécifique d'accès à des données hétérogènes avec ADO.</span><span class="sxs-lookup"><span data-stu-id="4ac67-104">[The OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md) shows a specific example of accessing heterogeneous data with ADO.</span></span> <span data-ttu-id="4ac67-105">Tandis que les exemples de cette section sont spécifiques à l'utilisation du fournisseur de publication Internet, les principes démontrés doivent être similaires lors de l'utilisation d'ADO avec d'autres fournisseurs pour les données hétérogènes, comme un fournisseur dans un magasin de courrier électronique.</span><span class="sxs-lookup"><span data-stu-id="4ac67-105">While the examples in this section will be specific to using the Internet Publishing Provider, the principles demonstrated should be similar when using ADO with other providers to heterogeneous data, such as a provider to an email store.</span></span>

## <a name="urls"></a><span data-ttu-id="4ac67-106">URL</span><span class="sxs-lookup"><span data-stu-id="4ac67-106">URLs</span></span>

<span data-ttu-id="4ac67-p102">Les URL peuvent être utilisées à la place des chaînes de connexion et du texte des commandes pour spécifier les sources de données et l'emplacement des fichiers et des répertoires. Vous pouvez les utiliser avec des objets [Connection](connection-object-ado.md) et **Recordset** existants ainsi qu'avec des objets **Record** et **Stream**.</span><span class="sxs-lookup"><span data-stu-id="4ac67-p102">Uniform Resource Locators (URLs) can be used as an alternative to connection strings and command text to specify data sources and the location of files and directories. You can use URLs with the existing [Connection](connection-object-ado.md) and **Recordset** objects as well as with the **Record** and **Stream** objects.</span></span>

<span data-ttu-id="4ac67-109">Pour plus d'informations sur l'utilisation des URL, consultez [URL absolues et relatives](absolute-and-relative-urls.md).</span><span class="sxs-lookup"><span data-stu-id="4ac67-109">For more information about using URLs, see [Absolute and Relative URLs](absolute-and-relative-urls.md).</span></span>

## <a name="record-fields"></a><span data-ttu-id="4ac67-110">Champs d'enregistrement</span><span class="sxs-lookup"><span data-stu-id="4ac67-110">Record Fields</span></span>

<span data-ttu-id="4ac67-p103">La différence qui distingue les données hétérogènes des données homogènes est qu’avec les premières, chaque ligne de données, ou objet **Record**, peut comporter des jeux de colonnes différents, ou objets **Field**, alors qu’avec les secondes, chaque ligne comporte le même jeu de colonnes. Pour plus d’informations sur des champs spécifiques au fournisseur pour la publication sur Internet, voir [Enregistrements et champs spécifiques au fournisseur](records-and-provider-supplied-fields.md).</span><span class="sxs-lookup"><span data-stu-id="4ac67-p103">The distinguishing difference between heterogeneous data and homogeneous data is that for the former, each row of data, or **Record**, can have a different set of columns, or **Fields**. For homogeneous data, each row has the same set of columns. For more information about the fields specific to the Internet Publishing Provider, see [Records and Provider-Supplied Fields](records-and-provider-supplied-fields.md).</span></span>

## <a name="appending-new-fields"></a><span data-ttu-id="4ac67-114">Ajout de nouveaux champs</span><span class="sxs-lookup"><span data-stu-id="4ac67-114">Appending New Fields</span></span>

<span data-ttu-id="4ac67-115">Plusieurs objets ADO ont été améliorés pour fonctionner avec les objets **Record** et **Stream**.</span><span class="sxs-lookup"><span data-stu-id="4ac67-115">Several ADO objects have been enhanced to work in conjunction with **Record** and **Stream** objects.</span></span>

  - <span data-ttu-id="4ac67-116">La méthode [Append](fields-collection-ado.md) de la collection [Fields](append-method-ado.md) permet de créer et d'ajouter un objet [Field](field-object-ado.md) à la collection et peut également spécifier la valeur de l'objet **Field**.</span><span class="sxs-lookup"><span data-stu-id="4ac67-116">The [Fields](fields-collection-ado.md) collection [Append](append-method-ado.md) method, which creates and adds a [Field](field-object-ado.md) object to the collection, can also specify the value of the **Field**.</span></span>

  - <span data-ttu-id="4ac67-117">La méthode [Update](update-method-ado.md) finalise l'ajout ou la suppression d'objets Field dans la collection.</span><span class="sxs-lookup"><span data-stu-id="4ac67-117">The [Update](update-method-ado.md) method finalizes the addition or deletion of fields to the collection.</span></span>

  - <span data-ttu-id="4ac67-118">Une autre solution plus rapide que l'utilisation de la méthode **Append** consiste à créer des champs simplement en affectant une valeur à un champ non défini ou précédemment supprimé.</span><span class="sxs-lookup"><span data-stu-id="4ac67-118">As a shortcut and alternative to the **Append** method, you may create fields by simply assigning a value to an undefined or previously deleted field.</span></span>

## <a name="see-also"></a><span data-ttu-id="4ac67-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ac67-119">See also</span></span>

- [<span data-ttu-id="4ac67-120">Rubriques de scénario de publication Internet</span><span class="sxs-lookup"><span data-stu-id="4ac67-120">Internet Publishing Scenario topics</span></span>](internet-publishing-scenario.md)
