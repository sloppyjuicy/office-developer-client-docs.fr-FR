---
title: FixMAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 32676003-ba32-886f-1185-4760cb0e30e3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3c064301a18a8adbfb6109170ed16cb6981d96c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783304"
---
# <a name="fixmapi"></a><span data-ttu-id="ddc36-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="ddc36-103">FixMAPI</span></span>

  
  
<span data-ttu-id="ddc36-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ddc36-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ddc36-105">Crée une copie de sauvegarde de la copie en cours de mapi32.dll sur le client ordinateur et restaure mapi32.dll avec la bibliothèque stub MAPI, mapistub.dll.</span><span class="sxs-lookup"><span data-stu-id="ddc36-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ddc36-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="ddc36-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ddc36-107">Exportés par :</span><span class="sxs-lookup"><span data-stu-id="ddc36-107">Exported by:</span></span>  <br/> |<span data-ttu-id="ddc36-108">Mapistub.dll</span><span class="sxs-lookup"><span data-stu-id="ddc36-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="ddc36-109">Appelée par :</span><span class="sxs-lookup"><span data-stu-id="ddc36-109">Called by:</span></span>  <br/> |<span data-ttu-id="ddc36-110">Client</span><span class="sxs-lookup"><span data-stu-id="ddc36-110">Client</span></span>  <br/> |
|<span data-ttu-id="ddc36-111">Implémentée par :</span><span class="sxs-lookup"><span data-stu-id="ddc36-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="ddc36-112">Windows</span><span class="sxs-lookup"><span data-stu-id="ddc36-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="ddc36-113">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="ddc36-113">Return values</span></span>

<span data-ttu-id="ddc36-114">Si la fonction réussit, la valeur de retour est une valeur non nulle.</span><span class="sxs-lookup"><span data-stu-id="ddc36-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="ddc36-115">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ddc36-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="ddc36-116">Pour obtenir des informations d’erreur étendues, appelez la fonction du Kit de développement logiciel (SDK) de Microsoft Windows, **[GetLastError](http://msdn.microsoft.com/fr-fr/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="ddc36-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](http://msdn.microsoft.com/fr-fr/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ddc36-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="ddc36-117">Remarks</span></span>

 <span data-ttu-id="ddc36-118">**FixMAPI** ne remplace pas le fichier mapi32.dll en cours si le fichier est marqué comme étant en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="ddc36-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="ddc36-119">**FixMAPI** ne remplace pas le fichier mapi32.dll en cours si Microsoft Exchange Server est installé sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ddc36-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="ddc36-120">**FixMAPI** lorsqu’une copie de sauvegarde de la copie en cours de mapi32.dll sur l’ordinateur, elle affecte à la copie de sauvegarde un nom différent de « mapi32.dll ».</span><span class="sxs-lookup"><span data-stu-id="ddc36-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="ddc36-121">Puis dirige les appels suivants destinés à cet assembly à la copie de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="ddc36-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ddc36-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddc36-122">See also</span></span>



[<span data-ttu-id="ddc36-123">KB 256946 : Vous recevez un message d’erreur de conflit programme lorsque vous démarrez Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="ddc36-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](http://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="ddc36-124">KB 228457 : Description de l’outil Fixmapi.exe inclus avec Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="ddc36-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](http://support.microsoft.com/kb/228457)

