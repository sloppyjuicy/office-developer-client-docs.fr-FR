---
title: Fonction COALESCE (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 92a7cc0a-1f9f-4969-8439-56a8d18e1347
description: Renvoie la première expression qui n'est pas NULL à partir d'une liste d'arguments.
ms.openlocfilehash: af309d2330f5c3b3999a4d99d8f2ab2d6d7d61db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282270"
---
# <a name="coalesce-function-access-custom-web-app"></a><span data-ttu-id="1d654-103">Fonction COALESCE (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="1d654-103">Coalesce function (Access custom web app)</span></span>

<span data-ttu-id="1d654-104">Renvoie la première expression qui n'est pas NULL à partir d'une liste d'arguments.</span><span class="sxs-lookup"><span data-stu-id="1d654-104">Returns the first expression that is not NULL from a list of arguments.</span></span>
  
> [!NOTE]
> <span data-ttu-id="1d654-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="1d654-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="1d654-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="1d654-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1d654-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d654-107">Syntax</span></span>

<span data-ttu-id="1d654-108">**COALESCE** (*Valeur*, [*valeur*],..., [*valeur*])</span><span class="sxs-lookup"><span data-stu-id="1d654-108">**Coalesce** (*Value*, [*Value*], …,[*Value*])</span></span> 
  
<span data-ttu-id="1d654-109">La fonction **COALESCE** contient les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="1d654-109">The **Coalesce** function contains the following arguments</span></span> 
  
|<span data-ttu-id="1d654-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="1d654-110">**Argument name**</span></span>|<span data-ttu-id="1d654-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="1d654-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="1d654-112">*Valeur*</span><span class="sxs-lookup"><span data-stu-id="1d654-112">*Value*</span></span>  <br/> |<span data-ttu-id="1d654-113">Expression.</span><span class="sxs-lookup"><span data-stu-id="1d654-113">An expression.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d654-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d654-114">Remarks</span></span>

<span data-ttu-id="1d654-115">Si tous les arguments sont NULL, **COALESCE** renvoie null.</span><span class="sxs-lookup"><span data-stu-id="1d654-115">If all arguments are NULL, **Coalesce** returns NULL.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1d654-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="1d654-116">Example</span></span>

<span data-ttu-id="1d654-117">L'expression suivante est utilisée comme règle de validation pour un tableau.</span><span class="sxs-lookup"><span data-stu-id="1d654-117">The following expression is used as the validation rule for a table.</span></span> <span data-ttu-id="1d654-118">L'expression garantit la saisie des entrées dans les champs prénom, nom, adresse de messagerie, téléphone mobile, téléphone professionnel, téléphone personnel et société avant la validation d'un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="1d654-118">The expression ensures that entries are made in the First Name, Last Name, Email, Mobile Phone, Work Phone, Home Phone, and Company fields before a record is committed.</span></span> <span data-ttu-id="1d654-119">Si l'un des champs répertoriés n'est pas renseigné, la fonction **COALESCE** renvoie la valeur null, ce qui enfreint la règle de validation.</span><span class="sxs-lookup"><span data-stu-id="1d654-119">If any of the listed fields are left blank, the **Coalesce** function returns Null, which violates the validation rule.</span></span> 
  
```vb
Coalesce([First Name],[Last Name],[Email],[Mobile Phone],[Work Phone],[Home Phone],[Company]) Is Not Null
```


