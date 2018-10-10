---
title: Append, méthode (Procédures ADOX)
TOCTitle: Append Method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5c1afc7aeea90fc152df7d8f7b1601bf3753b3a3
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469441"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="83e35-102">Append, méthode (Procédures ADOX)</span><span class="sxs-lookup"><span data-stu-id="83e35-102">Append Method (ADOX Procedures)</span></span>


<span data-ttu-id="83e35-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="83e35-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="83e35-104">Ajoute un nouvel objet [Procedure](procedure-object-adox.md) à la collection [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="83e35-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="83e35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83e35-105">Syntax</span></span>

<span data-ttu-id="83e35-106">*Procédures*. Ajouter le*nom*, *commande*</span><span class="sxs-lookup"><span data-stu-id="83e35-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="83e35-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83e35-107">Parameters</span></span>

  - <span data-ttu-id="83e35-108">*Name*</span><span class="sxs-lookup"><span data-stu-id="83e35-108">*Name*</span></span>

  - <span data-ttu-id="83e35-109">Valeur de type **String** qui spécifie le nom de la procédure à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="83e35-109">A **String** value that specifies the name of the procedure to create and append.</span></span>

  - <span data-ttu-id="83e35-110">*Command*</span><span class="sxs-lookup"><span data-stu-id="83e35-110">*Command*</span></span>

  - <span data-ttu-id="83e35-111">Objet ADO [Command](command-object-ado.md) qui représente la procédure à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="83e35-111">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>

## <a name="remarks"></a><span data-ttu-id="83e35-112">Notes</span><span class="sxs-lookup"><span data-stu-id="83e35-112">Remarks</span></span>

<span data-ttu-id="83e35-113">Crée une procédure dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="83e35-113">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="83e35-p101">Si le texte de commande spécifié par l'utilisateur représente une vue plutôt qu'une procédure, le comportement dépend du fournisseur utilisé. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="83e35-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>


> [!NOTE]
> <P><span data-ttu-id="83e35-116">Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode <STRONG>Append</STRONG> de la collection <STRONG>Procedures</STRONG> vous autorisera à spécifier une <STRONG>vue</STRONG> plutôt qu’une <STRONG>procédure</STRONG> dans le paramètre de <EM>commande</EM> .</span><span class="sxs-lookup"><span data-stu-id="83e35-116">When using the OLE DB Provider for Microsoft Jet, the <STRONG>Procedures</STRONG> collection <STRONG>Append</STRONG> method will allow you to specify a <STRONG>View</STRONG> rather than a <STRONG>Procedure</STRONG> in the <EM>Command</EM> parameter.</span></span> <span data-ttu-id="83e35-117">L'objet <STRONG>View</STRONG> sera ajouté à la source de données et à la collection <STRONG>Procedures</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="83e35-117">The <STRONG>View</STRONG> will be added to the data source and will be added to the <STRONG>Procedures</STRONG> collection.</span></span> <span data-ttu-id="83e35-118">Après cet <STRONG>ajout</STRONG> et en cas d'actualisation des collections <STRONG>Procedures</STRONG> et <STRONG>Views</STRONG>, l'objet <STRONG>View</STRONG> ne figurera plus dans la collection <STRONG>Procedures</STRONG> mais apparaîtra dans la collection <STRONG>Views</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="83e35-118">After the <STRONG>Append</STRONG>, if the <STRONG>Procedures</STRONG> and <STRONG>Views</STRONG> collections are refreshed, the <STRONG>View</STRONG> will no longer be in the <STRONG>Procedures</STRONG> collection and will appear in the <STRONG>Views</STRONG> collection.</span></span></P>


