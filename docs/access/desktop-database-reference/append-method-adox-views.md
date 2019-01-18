---
title: Append, méthode (Vues ADOX)
TOCTitle: Append method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9e1a6e14542f267af6a9f5bc58bb2d75a11aac77
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716152"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="a678d-102">Append, méthode (Vues ADOX)</span><span class="sxs-lookup"><span data-stu-id="a678d-102">Append method (ADOX Views)</span></span>

<span data-ttu-id="a678d-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a678d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a678d-104">Crée un objet [View](view-object-adox.md) et l'ajoute à la collection [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="a678d-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a678d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a678d-105">Syntax</span></span>

<span data-ttu-id="a678d-106">*Affichages*. Ajouter le*nom*, *commande*</span><span class="sxs-lookup"><span data-stu-id="a678d-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="a678d-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="a678d-107">Parameters</span></span>

|<span data-ttu-id="a678d-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="a678d-108">Parameter</span></span>|<span data-ttu-id="a678d-109">Description</span><span class="sxs-lookup"><span data-stu-id="a678d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="a678d-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="a678d-110">*Name*</span></span> |<span data-ttu-id="a678d-111">Valeur de type **String** qui spécifie le nom de la vue à créer.</span><span class="sxs-lookup"><span data-stu-id="a678d-111">A **String** value that specifies the name of the view to create.</span></span>|
|<span data-ttu-id="a678d-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="a678d-112">*Command*</span></span> |<span data-ttu-id="a678d-113">Objet [Command](command-object-ado.md) ADO qui représente la vue à créer.</span><span class="sxs-lookup"><span data-stu-id="a678d-113">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>|

## <a name="remarks"></a><span data-ttu-id="a678d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="a678d-114">Remarks</span></span>

<span data-ttu-id="a678d-115">Crée une vue dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="a678d-115">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="a678d-p101">Si le texte de commande spécifié par l'utilisateur représente une procédure plutôt qu'une vue, le comportement dépend du fournisseur. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="a678d-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="a678d-118">Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode **Append** de collection **Views** vous autorisera à spécifier une **procédure** plutôt qu’une **vue** dans le paramètre de *commande* .</span><span class="sxs-lookup"><span data-stu-id="a678d-118">When using the OLE DB Provider for Microsoft Jet, the **Views** collection **Append** method will allow you to specify a **Procedure** rather than a **View** in the *Command* parameter.</span></span> <span data-ttu-id="a678d-119">L'objet **Procedure** sera ajouté à la source de données et à la collection **Views**.</span><span class="sxs-lookup"><span data-stu-id="a678d-119">The **Procedure** will be added to the data source and will be added to the **Views** collection.</span></span> <span data-ttu-id="a678d-120">Après cet **ajout** et en cas d'actualisation des collections **Procedures** et **Views**, l'objet **Procedure** ne figurera plus dans la collection **Views** mais apparaîtra dans la collection **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="a678d-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **Procedure** will no longer be in the **Views** collection and will appear in the **Procedures** collection.</span></span>


