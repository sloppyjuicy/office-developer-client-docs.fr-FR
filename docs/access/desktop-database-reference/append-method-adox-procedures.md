---
title: Append, méthode (Procédures ADOX)
TOCTitle: Append method (ADOX Procedures)
ms:assetid: a93b31bb-e41a-5152-abe7-dd7c2b2fcd0a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249783(v=office.15)
ms:contentKeyID: 48546919
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a2de9dc7d8dccfc4107dbd802c4013ac794acf61
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297080"
---
# <a name="append-method-adox-procedures"></a><span data-ttu-id="4915d-102">Append, méthode (Procédures ADOX)</span><span class="sxs-lookup"><span data-stu-id="4915d-102">Append method (ADOX Procedures)</span></span>

<span data-ttu-id="4915d-103">**S’applique à** : Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4915d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4915d-104">Ajoute un nouvel objet [Procedure](procedure-object-adox.md) à la collection [Procedures](procedures-collection-adox.md).</span><span class="sxs-lookup"><span data-stu-id="4915d-104">Adds a new [Procedure](procedure-object-adox.md) object to the [Procedures](procedures-collection-adox.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="4915d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4915d-105">Syntax</span></span>

<span data-ttu-id="4915d-106">*Procédures*. Append *Name*, *Command*</span><span class="sxs-lookup"><span data-stu-id="4915d-106">*Procedures*.Append *Name*, *Command*</span></span>

## <a name="parameters"></a><span data-ttu-id="4915d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4915d-107">Parameters</span></span>

|<span data-ttu-id="4915d-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="4915d-108">Parameter</span></span>|<span data-ttu-id="4915d-109">Description</span><span class="sxs-lookup"><span data-stu-id="4915d-109">Description</span></span>|
|:--------|:----------|
|<span data-ttu-id="4915d-110">*Name*</span><span class="sxs-lookup"><span data-stu-id="4915d-110">*Name*</span></span> |<span data-ttu-id="4915d-111">Valeur de type **String** qui spécifie le nom de la procédure à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="4915d-111">A **String** value that specifies the name of the procedure to create and append.</span></span>|
|<span data-ttu-id="4915d-112">*Command*</span><span class="sxs-lookup"><span data-stu-id="4915d-112">*Command*</span></span> |<span data-ttu-id="4915d-113">Objet ADO [Command](command-object-ado.md) qui représente la procédure à créer et à ajouter.</span><span class="sxs-lookup"><span data-stu-id="4915d-113">An ADO [Command](command-object-ado.md) object that represents the procedure to create and append.</span></span>|

## <a name="remarks"></a><span data-ttu-id="4915d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4915d-114">Remarks</span></span>

<span data-ttu-id="4915d-115">Crée une procédure dans la source de données avec le nom et les attributs spécifiés dans l'objet **Command**.</span><span class="sxs-lookup"><span data-stu-id="4915d-115">Creates a new procedure in the data source with the name and attributes specified in the **Command** object.</span></span>

<span data-ttu-id="4915d-p101">Si le texte de commande spécifié par l'utilisateur représente une vue plutôt qu'une procédure, le comportement dépend du fournisseur utilisé. La méthode **Append** échoue si le fournisseur ne prend pas en charge les commandes persistantes.</span><span class="sxs-lookup"><span data-stu-id="4915d-p101">If the command text that the user specifies represents a view rather than a procedure, the behavior is dependent upon the provider being used. **Append** will fail if the provider does not support persisting commands.</span></span>

> [!NOTE]
> <span data-ttu-id="4915d-p102">En cas d'utilisation du fournisseur OLE DB pour Microsoft Jet, la méthode **Append** de la collection **Procedures** vous permet de spécifier un objet **View** plutôt qu'un objet **Procedure** dans le paramètre *Command*. L'objet **View** sera ajouté à la source de données et à la collection **Procedures**. Après cet **ajout** et en cas d'actualisation des collections **Procedures** et **Views**, l'objet **View** ne figurera plus dans la collection **Procedures** mais apparaîtra dans la collection **Views**.</span><span class="sxs-lookup"><span data-stu-id="4915d-p102">When using the OLE DB Provider for Microsoft Jet, the **Procedures** collection **Append** method will allow you to specify a **View** rather than a **Procedure** in the *Command* parameter. The **View** will be added to the data source and will be added to the **Procedures** collection. After the **Append**, if the **Procedures** and **Views** collections are refreshed, the **View** will no longer be in the **Procedures** collection and will appear in the **Views** collection.</span></span>


