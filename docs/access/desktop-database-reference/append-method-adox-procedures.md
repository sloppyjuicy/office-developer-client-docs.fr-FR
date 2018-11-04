---
title: Append, méthode (Procédures ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 65a8e0b805bf964ae60bd9de25fc45cf5b04482f
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2018
ms.locfileid: "25949690"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="9a3c9-102">Append, méthode (Procédures ADOX)</span><span class="sxs-lookup"><span data-stu-id="9a3c9-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="9a3c9-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9a3c9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9a3c9-104">Ajoute un nouvel objet [Procedure](procedure-object-adox.md) à la collection [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="9a3c9-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a3c9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a3c9-105">Syntax</span></span>

<span data-ttu-id="9a3c9-106">*Procédures*. Ajouter le*nom*, *commande*</span><span class="sxs-lookup"><span data-stu-id="9a3c9-106">*Procedures*.Append*Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="9a3c9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a3c9-107">Parameters</span></span>

|<span data-ttu-id="9a3c9-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="9a3c9-108">Parameter</span></span>|<span data-ttu-id="9a3c9-109">Description</span><span class="sxs-lookup"><span data-stu-id="9a3c9-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="9a3c9-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="9a3c9-110">*Name*</span></span> |<span data-ttu-id="9a3c9-111">Valeur de type **String** qui spécifie le nom de la procédure à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="9a3c9-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="9a3c9-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="9a3c9-112">*Command*</span></span> |<span data-ttu-id="9a3c9-113">Objet ADO [Command](command-object-ado.md) qui représente la procédure à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="9a3c9-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="9a3c9-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9a3c9-114">Remarks</span></span>

<span data-ttu-id="9a3c9-115">Crée une procédure dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="9a3c9-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="9a3c9-p101">Si le texte de commande spécifié par l'utilisateur représente une vue plutôt qu'une procédure, le comportement dépend du fournisseur utilisé. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="9a3c9-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="9a3c9-118">Lorsque vous utilisez le fournisseur OLE DB pour Microsoft Jet, la méthode **Append** de la collection **Procedures** vous autorisera à spécifier une **vue** plutôt qu’une **procédure** dans le paramètre de *commande* .</span><span class="sxs-lookup"><span data-stu-id="9a3c9-118">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter.</span></span> <span data-ttu-id="9a3c9-119">L'objet **View** sera ajouté à la source de données et à la collection **Procedures**.</span><span class="sxs-lookup"><span data-stu-id="9a3c9-119">The **View** will be added to the data source and will be added to the **Procedures** collection.</span></span> <span data-ttu-id="9a3c9-120">Après cet **ajout** et en cas d'actualisation des collections **Procedures** et **Views**, l'objet **View** ne figurera plus dans la collection **Procedures** mais apparaîtra dans la collection **Views**.</span><span class="sxs-lookup"><span data-stu-id="9a3c9-120">After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


