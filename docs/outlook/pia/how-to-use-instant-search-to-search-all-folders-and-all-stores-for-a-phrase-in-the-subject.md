---
title: Utilisation de la recherche instantanée pour rechercher une expression employée dans l’objet dans tous les dossiers et toutes les banques
TOCTitle: Use instant search to search all folders and all stores for a phrase in the subject
ms:assetid: d3152bfa-6e7d-4b68-8c7e-e2e155a92b49
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424478(v=office.15)
ms:contentKeyID: 55119923
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 07b0ba7a1d488dc1c7e1fcf0e9ae487b04b88755
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335370"
---
# <a name="use-instant-search-to-search-all-folders-and-all-stores-for-a-phrase-in-the-subject"></a><span data-ttu-id="bc0e3-102">Utiliser la recherche instantanée pour effectuer une recherche dans tous les dossiers et tous les magasins pour une expression dans l’objet</span><span class="sxs-lookup"><span data-stu-id="bc0e3-102">Use instant search to search all folders and all stores for a phrase in the subject</span></span>

<span data-ttu-id="bc0e3-103">Cet exemple utilise la recherche instantanée pour rechercher une phrase dans l'objet à travers tous les dossiers et toutes les banques, puis affiche les éléments dans une fenêtre d'explorateur.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-103">This example uses Instant Search to search all folders and all stores for a phrase in the subject, and then displays the items in an explorer window.</span></span>

## <a name="example"></a><span data-ttu-id="bc0e3-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="bc0e3-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="bc0e3-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="bc0e3-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="bc0e3-106">La recherche instantanée est une fonctionnalité de Microsoft Outlook qui permet d’effectuer des recherches en émettant des requêtes qui renvoient des résultats en fonction du contenu.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-106">Instant Search is a feature of Microsoft Outlook that enables you to search by issuing queries that return results based on the content.</span></span> <span data-ttu-id="bc0e3-107">Une fois que votre requête a été traitée, les résultats peuvent être retournés dans différents objets, y compris l'objet [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) , la collection [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) et l'objet [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) .</span><span class="sxs-lookup"><span data-stu-id="bc0e3-107">Once your query has been processed, the results can be returned in a variety of objects, including the [Table](https://msdn.microsoft.com/library/bb652856\(v=office.15\)) object, the [Items](https://msdn.microsoft.com/library/bb645287\(v=office.15\)) collection, and the [Search](https://msdn.microsoft.com/library/bb612611\(v=office.15\)) object.</span></span> <span data-ttu-id="bc0e3-108">Vous pouvez écrire du code qui utilise la recherche instantanée à l'aide de la syntaxe AQS (Advanced Query Syntax), qui est disponible avec Microsoft Windows Desktop Search.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-108">You can write code that uses Instant Search by using the Advanced Query Syntax (AQS) that is offered by Microsoft Windows Desktop Search.</span></span> <span data-ttu-id="bc0e3-109">AQS est un des trois langages de requête pris en charge par Outlook.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-109">AQS is one of three query languages that Outlook supports.</span></span> <span data-ttu-id="bc0e3-110">Il est puissant, mais limité à la méthode [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) de l’objet [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="bc0e3-110">It is powerful, but limited to the [Search(String, OlSearchScope)](https://msdn.microsoft.com/library/bb610561\(v=office.15\)) method of the [Explorer](https://msdn.microsoft.com/library/bb623678\(v=office.15\)) object.</span></span> <span data-ttu-id="bc0e3-111">Vous ne pouvez pas utiliser AQS pour fournir une restriction pour des objets **Table** ou **Item**.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-111">You cannot use AQS to provide a restriction for **Table** or **Item** objects.</span></span> <span data-ttu-id="bc0e3-112">En outre, les résultats renvoyés par une requête AQS peuvent être affichés uniquement dans l’interface utilisateur Outlook.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-112">In addition, the results returned by an AQS query can be displayed only in the Outlook user interface.</span></span> <span data-ttu-id="bc0e3-113">Le tableau suivant répertorie les trois langages de requête pris en charge par Outlook ; cette rubrique ne montrera cependant que l’utilisation d’AQS.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-113">The following table lists the three query languages that Outlook supports; however, this topic will illustrate the use of only AQS.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc0e3-114">Langage de requête</span><span class="sxs-lookup"><span data-stu-id="bc0e3-114">Query language</span></span></p></th>
<th><p><span data-ttu-id="bc0e3-115">Description</span><span class="sxs-lookup"><span data-stu-id="bc0e3-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc0e3-116">AQS</span><span class="sxs-lookup"><span data-stu-id="bc0e3-116">AQS</span></span></p></td>
<td><p><span data-ttu-id="bc0e3-117">AQS est utilisé par Windows Desktop Search et est le langage de recherche pour la fonction de recherche instantanée dans Outlook.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-117">AQS is used by Windows Desktop Search and is the query language for the Instant Search feature in Outlook.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc0e3-118">DASL</span><span class="sxs-lookup"><span data-stu-id="bc0e3-118">DASL</span></span></p></td>
<td><p><span data-ttu-id="bc0e3-p102">Le langage de recherche DASL (DAV Search and Locating) est basé sur l’implémentation Microsoft Exchange de DASL dans Outlook. DASL peut être utilisé pour retourner des résultats dans l’objet <b>Table</b>. </span><span class="sxs-lookup"><span data-stu-id="bc0e3-p102">DAV Search and Locating (DASL) query language is based on the Microsoft Exchange implementation of DASL in Outlook. DASL can be used to return results in the <b>Table</b> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc0e3-121">Jet</span><span class="sxs-lookup"><span data-stu-id="bc0e3-121">Jet</span></span></p></td>
<td><p><span data-ttu-id="bc0e3-p103">Le langage de requête Jet offre un langage de requête simple pour Outlook, et il est basé sur Microsoft Jet Expression Service. Jet est utilisé pour créer des chaînes de filtre pour les méthodes <b>Restrict</b> de la collection <b>Items</b> et l’objet <b>Table</b>.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-p103">Jet query language provides a simple query language for Outlook, and is based on the Microsoft Jet Expression Service. Jet is used to create filter strings for the <b>Restrict</b> methods of the <b>Items</b> collection and the <b>Table</b> object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bc0e3-124">Dans l’exemple de code suivant, DemoInstantSearch obtient tous les dossiers de messagerie électronique de tous les magasins où l’indexation est activée à l’aide de la propriété [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) de l’objet [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="bc0e3-124">In the following code example, DemoInstantSearch gets all mail folders in all stores where indexing is enabled by using the [IsInstantSearchEnabled](https://msdn.microsoft.com/library/bb609793\(v=office.15\)) property of the [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object.</span></span> <span data-ttu-id="bc0e3-125">Il utilise ensuite la méthode **Search** de l’objet **Explorer** pour filtrer tous les éléments qui contiennent la phrase exacte « Office 2007 » dans l’objet et qui ont été reçus au cours du mois dernier.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-125">It then uses the **Search** method of the **Explorer** object to filter for all items that contain the exact phrase “Office 2007” in the subject and that have been received in the last month.</span></span> <span data-ttu-id="bc0e3-126">Enfin, les résultats de la recherche sont affichés dans une fenêtre distincte de l’explorateur.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-126">The results of the search are finally displayed in a separate explorer window.</span></span>

<span data-ttu-id="bc0e3-127">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-127">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="bc0e3-128">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-128">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="bc0e3-129">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="bc0e3-129">The following line of code shows how to do the import and assignment in C\#.</span></span>

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void DemoInstantSearch()
{
    if (Application.Session.DefaultStore.IsInstantSearchEnabled)
    {
        Outlook.Explorer explorer = Application.Explorers.Add(
            Application.Session.GetDefaultFolder(
            Outlook.OlDefaultFolders.olFolderInbox)
            as Outlook.Folder,
            Outlook.OlFolderDisplayMode.olFolderDisplayNormal);
        string filter = "subject:" +
            "\"" + "Office 2007" + "\"" +
            " received:(last month)";
        explorer.Search(filter,
            Outlook.OlSearchScope.olSearchScopeAllFolders);
        explorer.Display();
    }
}
```

## <a name="see-also"></a><span data-ttu-id="bc0e3-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bc0e3-130">See also</span></span>

- [<span data-ttu-id="bc0e3-131">Rechercher et filtrer</span><span class="sxs-lookup"><span data-stu-id="bc0e3-131">Search and filter</span></span>](search-and-filter.md)

