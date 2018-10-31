---
title: Append, méthode (Vues ADOX)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ca51537c78dfc07a6cd3560bba7154f6b56ef31f
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861210"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="a1d5f-102">Append, méthode (Vues ADOX)</span><span class="sxs-lookup"><span data-stu-id="a1d5f-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="a1d5f-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a1d5f-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a1d5f-104">Crée un objet [View](view-object-adox.md) et l'ajoute à la collection [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="a1d5f-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1d5f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1d5f-105">Syntax</span></span>

<span data-ttu-id="a1d5f-106">*Affichages*. Ajouter le*nom*, *commande*</span><span class="sxs-lookup"><span data-stu-id="a1d5f-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="a1d5f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1d5f-107">Parameters</span></span>

  - <span data-ttu-id="a1d5f-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="a1d5f-108">*Name*</span></span>

  - <span data-ttu-id="a1d5f-109">Valeur de type **String** qui spécifie le nom de la vue à créer.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="a1d5f-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="a1d5f-110">*Command*</span></span>

  - <span data-ttu-id="a1d5f-111">Objet [Command](command-object-ado.md) ADO qui représente la vue à créer.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1d5f-112">Notes</span><span class="sxs-lookup"><span data-stu-id="a1d5f-112">Remarks</span></span>

<span data-ttu-id="a1d5f-113">Crée une vue dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="a1d5f-p101">Si le texte de commande spécifié par l'utilisateur représente une procédure plutôt qu'une vue, le comportement dépend du fournisseur. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <span data-ttu-id="a1d5f-116">Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode **Append** de collection **Views** vous autorisera à spécifier une **procédure** plutôt qu’une **vue** dans le paramètre de *commande* .</span><span class="sxs-lookup"><span data-stu-id="a1d5f-116">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="a1d5f-117">L'objet **Procedure** sera ajouté à la source de données et à la collection **Views**.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-117">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="a1d5f-118">Après cet **ajout** et en cas d'actualisation des collections **Procedures** et **Views**, l'objet **Procedure** ne figurera plus dans la collection **Views** mais apparaîtra dans la collection **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="a1d5f-118">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


