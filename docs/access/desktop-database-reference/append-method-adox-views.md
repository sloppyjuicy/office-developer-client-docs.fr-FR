---
title: Append, méthode (Vues ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ccba425e74321f4ab760e9ddc4a722295290ffd1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925155"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="fc3b1-102">Append, méthode (Vues ADOX)</span><span class="sxs-lookup"><span data-stu-id="fc3b1-102">Append method (ADOX Views)</span></span>


<span data-ttu-id="fc3b1-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fc3b1-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="fc3b1-104">Crée un objet [View](view-object-adox.md) et l'ajoute à la collection [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="fc3b1-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc3b1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc3b1-105">Syntax</span></span>

<span data-ttu-id="fc3b1-106">*Affichages*. Ajouter le*nom*, *commande*</span><span class="sxs-lookup"><span data-stu-id="fc3b1-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="fc3b1-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc3b1-107">Parameters</span></span>

  - <span data-ttu-id="fc3b1-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="fc3b1-108">*Name*</span></span>

  - <span data-ttu-id="fc3b1-109">Valeur de type **String** qui spécifie le nom de la vue à créer.</span><span class="sxs-lookup"><span data-stu-id="fc3b1-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="fc3b1-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="fc3b1-110">*Command*</span></span>

  - <span data-ttu-id="fc3b1-111">Objet [Command](command-object-ado.md) ADO qui représente la vue à créer.</span><span class="sxs-lookup"><span data-stu-id="fc3b1-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc3b1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fc3b1-112">Remarks</span></span>

<span data-ttu-id="fc3b1-113">Crée une vue dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="fc3b1-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="fc3b1-p101">Si le texte de commande spécifié par l'utilisateur représente une procédure plutôt qu'une vue, le comportement dépend du fournisseur. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="fc3b1-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="fc3b1-116">Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode **Append** de collection **Views** vous autorisera à spécifier une **procédure** plutôt qu’une **vue** dans le paramètre de *commande* .</span><span class="sxs-lookup"><span data-stu-id="fc3b1-116">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="fc3b1-117">L'objet **Procedure** sera ajouté à la source de données et à la collection **Views**.</span><span class="sxs-lookup"><span data-stu-id="fc3b1-117">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="fc3b1-118">Après cet **ajout** et en cas d'actualisation des collections **Procedures** et **Views**, l'objet **Procedure** ne figurera plus dans la collection **Views** mais apparaîtra dans la collection **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="fc3b1-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


