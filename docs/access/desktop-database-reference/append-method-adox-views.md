---
title: Append, méthode (Vues ADOX)
TOCTitle: Append Method (ADOX Views)
ms:assetid: 202f1d0a-dc5d-84e5-daf3-3212e5bc6088
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248985(v=office.15)
ms:contentKeyID: 48543655
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 106dd9d72cb350422f00da05859bc096cb2b52e9
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470822"
---
# <a name="append-method-adox-views"></a><span data-ttu-id="fe494-102">Append, méthode (Vues ADOX)</span><span class="sxs-lookup"><span data-stu-id="fe494-102">Append Method (ADOX Views)</span></span>


<span data-ttu-id="fe494-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe494-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="fe494-104">Crée un objet [View](view-object-adox.md) et l'ajoute à la collection [Views](views-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="fe494-104">Creates a new [View](view-object-adox.md) object and appends it to the [Views](views-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe494-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe494-105">Syntax</span></span>

<span data-ttu-id="fe494-106">*Affichages*. Ajouter le*nom*, *commande*</span><span class="sxs-lookup"><span data-stu-id="fe494-106">*Views*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="fe494-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe494-107">Parameters</span></span>

  - <span data-ttu-id="fe494-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="fe494-108">*Name*</span></span>

  - <span data-ttu-id="fe494-109">Valeur de type **String** qui spécifie le nom de la vue à créer.</span><span class="sxs-lookup"><span data-stu-id="fe494-109">A **String** value that specifies the name of the view to create.</span></span>

  - <span data-ttu-id="fe494-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="fe494-110">*Command*</span></span>

  - <span data-ttu-id="fe494-111">Objet [Command](command-object-ado.md) ADO qui représente la vue à créer.</span><span class="sxs-lookup"><span data-stu-id="fe494-111">An ADO [Command](command-object-ado.md) object that represents the view to create.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe494-112">Notes</span><span class="sxs-lookup"><span data-stu-id="fe494-112">Remarks</span></span>

<span data-ttu-id="fe494-113">Crée une vue dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="fe494-113">Creates a new view in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="fe494-p101">Si le texte de commande spécifié par l'utilisateur représente une procédure plutôt qu'une vue, le comportement dépend du fournisseur. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="fe494-p101">If the command text that the user specifies represents a procedure rather than a view, the behavior is dependent upon the provider. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="fe494-116">Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode <STRONG>Append</STRONG> de collection <STRONG>Views</STRONG> vous autorisera à spécifier une <STRONG>procédure</STRONG> plutôt qu’une <STRONG>vue</STRONG> dans le paramètre de <EM>commande</EM> .</span><span class="sxs-lookup"><span data-stu-id="fe494-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Views</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>Procedure</STRONG> rather than a <STRONG>View</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="fe494-117">L'objet <STRONG>Procedure</STRONG> sera ajouté à la source de données et à la collection <STRONG>Views</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="fe494-117">The <STRONG>Procedure</STRONG> will be added to the data source and will be added to the <STRONG>Views</STRONG> collection.</span></span> <span data-ttu-id="fe494-118">Après cet <STRONG>ajout</STRONG> et en cas d'actualisation des collections <STRONG>Procedures</STRONG> et <STRONG>Views</STRONG>, l'objet <STRONG>Procedure</STRONG> ne figurera plus dans la collection <STRONG>Views</STRONG> mais apparaîtra dans la collection <STRONG>Procedures</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="fe494-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>Procedure</STRONG> will no longer be in the <STRONG>Views</STRONG> collection and will appear in the <STRONG>Procedures</STRONG> collection.</span></span></P>


