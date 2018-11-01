---
title: Programmation ADO/WFC
TOCTitle: ADO/WFC Programming
ms:assetid: fc438cc2-00b9-9590-6e0d-a865001ccf2f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250293(v=office.15)
ms:contentKeyID: 48548887
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ea531f484ad75de268f0d4fb38a10e617c1851e6
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25884631"
---
# <a name="adowfc-programming"></a><span data-ttu-id="ac914-102">Programmation ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ac914-102">ADO/WFC Programming</span></span>


<span data-ttu-id="ac914-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ac914-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ac914-p101">ADO a été étendu pour Microsoft Visual J++ 6.0 afin de fonctionner avec Windows Foundation Classes (WFC) de la façon suivante. Un ensemble de classes Java a été implémenté pour étendre les interfaces ADO et créer des notifications destinées au programmeur Java ; les classes Java exposent également des fonctions qui retournent les types Java à l'utilisateur. Pour améliorer les performances, la classe Java accède directement aux types de données natifs dans l'objet rowset OLE DB et les retourne au programmeur Java en tant que types Java sans les avoir au préalable convertis en type variant. ADO a également été étendu de manière à utiliser des notifications d'événements dans l'infrastructure WFC.</span><span class="sxs-lookup"><span data-stu-id="ac914-p101">For Microsoft Visual J++ 6.0, ADO has been extended to work with Windows Foundation Classes (WFC) in the following ways. First, a set of Java classes has been implemented that extends the ADO interfaces and creates notifications interesting to the Java programmer; the Java classes also expose functions that return Java types to the user. To improve performance, the Java class directly accesses the native data types in the OLE DB rowset object, and returns them to the Java programmer as Java types without first converting them to and from a variant. ADO has also been extended to work with event notifications in the WFC framework.</span></span>

<span data-ttu-id="ac914-p102">ADO pour Windows Foundation Classes (ADO/WFC) prend en charge toutes les méthodes et propriétés ainsi que tous les objets et événements ADO standard. En revanche, les opérations qui requièrent un variant en tant que paramètre et sont très performantes dans Microsoft Visual Basic, sont moins performantes dans un langage tel que Visual J++. Pour cette raison, ADO/WFC comporte également des fonctions d'accesseur sur l'objet [Field](field-object-ado.md) qui prennent les types de données Java natifs plutôt que les types de données variant.</span><span class="sxs-lookup"><span data-stu-id="ac914-p102">ADO for Windows Foundation Classes (ADO/WFC) supports all the standard ADO methods, properties, objects, and events. However, operations that require a variant as a parameter and show excellent performance in a language such as Microsoft Visual Basic, display lesser performance in a language such as Visual J++. For that reason, ADO/WFC also provides accessor functions on the [Field](field-object-ado.md) object that take native Java data types instead of the variant data type.</span></span>

<span data-ttu-id="ac914-111">Pour des informations plus détaillées dans la documentation ADO sur les packages ADO/WFC, consultez [Index de la syntaxe ADO/WFC](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="ac914-111">For more detailed information within the ADO documentation about ADO/WFC packages, see [the ADO/WFC Syntax Index](https://msdn.microsoft.com/library/jj250066\(v=office.15\)).</span></span>

## <a name="referencing-the-library"></a><span data-ttu-id="ac914-112">Référence de la bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ac914-112">Referencing the Library</span></span>

<span data-ttu-id="ac914-113">Pour importer les classes de données ADO/WFC dans votre projet, ajoutez la ligne suivante dans le code :</span><span class="sxs-lookup"><span data-stu-id="ac914-113">To import the ADO/WFC data classes into your project, include the following line in your code:</span></span>

```java 
 
import com.ms.wfc.data.*; 
```

