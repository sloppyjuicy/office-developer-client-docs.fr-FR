---
title: Fusion de fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Renvoie la première expression n’est pas NULL à partir d’une liste d’arguments.
ms.openlocfilehash: cfe6f59c22a89b2a6d211e5f05c2dbf275d8da11
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781824"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="e765d-103">Fusion de fonction (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="e765d-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="e765d-104">Renvoie la première expression n’est pas NULL à partir d’une liste d’arguments.</span><span class="sxs-lookup"><span data-stu-id="e765d-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e765d-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="e765d-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="e765d-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="e765d-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e765d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e765d-107">Syntax</span></span>

<span data-ttu-id="e765d-108">**Fusion** (*Valeur*, [*valeur*],..., [*valeur*])</span><span class="sxs-lookup"><span data-stu-id="e765d-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="e765d-109">La fonction de **fusion** contient les arguments suivants</span><span class="sxs-lookup"><span data-stu-id="e765d-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="e765d-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="e765d-110">**Argument name**</span></span>|<span data-ttu-id="e765d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e765d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e765d-112">*Valeur*</span><span class="sxs-lookup"><span data-stu-id="e765d-112">*Value*</span></span>  <br/> |<span data-ttu-id="e765d-113">Une expression.</span><span class="sxs-lookup"><span data-stu-id="e765d-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e765d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e765d-114">Remarks</span></span>

<span data-ttu-id="e765d-115">Si tous les arguments sont NULL, **fusion** renvoie la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="e765d-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e765d-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="e765d-116">Example</span></span>

<span data-ttu-id="e765d-117">L’expression suivante est utilisée en tant que la règle de validation pour une table.</span><span class="sxs-lookup"><span data-stu-id="e765d-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="e765d-118">L’expression garantit que les entrées sont effectuées dans les champs Prénom, dernier nom, courrier électronique, téléphone Mobile, travail, accueil téléphone, et compagnie de téléphone avant d’un enregistrement est validé.</span><span class="sxs-lookup"><span data-stu-id="e765d-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="e765d-119">Si un des champs répertoriés sont vides, la fonction de **fusion** renvoie la valeur Null, ce qui enfreint la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="e765d-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


