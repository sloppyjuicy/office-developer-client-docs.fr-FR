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
ms.openlocfilehash: 2aeca1a65a859ac9502995a463bc4869609bcd15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334960"
---
# <a name="fixmapi"></a><span data-ttu-id="de119-103">FixMAPI</span><span class="sxs-lookup"><span data-stu-id="de119-103">FixMAPI</span></span>

  
  
<span data-ttu-id="de119-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de119-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de119-105">Effectue une copie de sauvegarde de la copie actuelle de Mapi32. dll sur l'ordinateur client et restaure Mapi32. dll à l'aide de la bibliothèque de stubs MAPI, mapistub. dll.</span><span class="sxs-lookup"><span data-stu-id="de119-105">Makes a backup copy of the current copy of mapi32.dll on the client computer, and restores mapi32.dll with the MAPI stub library, mapistub.dll.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="de119-106">Informations rapides</span><span class="sxs-lookup"><span data-stu-id="de119-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de119-107">Exporté par:</span><span class="sxs-lookup"><span data-stu-id="de119-107">Exported by:</span></span>  <br/> |<span data-ttu-id="de119-108">mapistub. dll</span><span class="sxs-lookup"><span data-stu-id="de119-108">mapistub.dll</span></span>  <br/> |
|<span data-ttu-id="de119-109">Appelé par :</span><span class="sxs-lookup"><span data-stu-id="de119-109">Called by:</span></span>  <br/> |<span data-ttu-id="de119-110">Client</span><span class="sxs-lookup"><span data-stu-id="de119-110">Client</span></span>  <br/> |
|<span data-ttu-id="de119-111">Implémenté par :</span><span class="sxs-lookup"><span data-stu-id="de119-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="de119-112">Windows</span><span class="sxs-lookup"><span data-stu-id="de119-112">Windows</span></span>  <br/> |
   
```cpp
DWORD STDAPICALLTYPE FixMAPI(void); 
```

## <a name="return-values"></a><span data-ttu-id="de119-113">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="de119-113">Return values</span></span>

<span data-ttu-id="de119-114">Si la fonction réussit, la valeur renvoyée est une valeur non nulle.</span><span class="sxs-lookup"><span data-stu-id="de119-114">If the function succeeds, the return value is a non-zero value.</span></span>
  
<span data-ttu-id="de119-115">Si la fonction échoue, la valeur renvoyée est zéro.</span><span class="sxs-lookup"><span data-stu-id="de119-115">If the function fails, the return value is zero.</span></span> <span data-ttu-id="de119-116">Pour obtenir des informations détaillées sur les erreurs, appelez la fonction de kit de développement logiciel (SDK) de Microsoft Windows, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span><span class="sxs-lookup"><span data-stu-id="de119-116">To get extended error information, call the Microsoft Windows Software Development Kit (SDK) function, **[GetLastError](https://msdn.microsoft.com/library/ms679360.aspx)**.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="de119-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="de119-117">Remarks</span></span>

 <span data-ttu-id="de119-118">**Fixmapi** ne remplace pas le fichier Mapi32. dll actuel si le fichier est marqué en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="de119-118">**FixMAPI** does not replace the current mapi32.dll file if the file is marked as read-only.</span></span> 
  
 <span data-ttu-id="de119-119">**Fixmapi** ne remplace pas le fichier Mapi32. dll actuel si Microsoft Exchange Server est installé sur l'ordinateur.</span><span class="sxs-lookup"><span data-stu-id="de119-119">**FixMAPI** does not replace the current mapi32.dll if Microsoft Exchange Server is installed on the computer.</span></span> 
  
<span data-ttu-id="de119-120">Lorsque **Fixmapi** crée une copie de sauvegarde de la copie actuelle de Mapi32. dll sur l'ordinateur, il affecte à la copie de sauvegarde un nom différent de «Mapi32. dll».</span><span class="sxs-lookup"><span data-stu-id="de119-120">When **FixMAPI** makes a backup copy of the current copy of mapi32.dll on the computer, it assigns the backup copy a name different from "mapi32.dll".</span></span> <span data-ttu-id="de119-121">Il dirige ensuite les appels suivants destinés à cet assembly vers la copie de sauvegarde.</span><span class="sxs-lookup"><span data-stu-id="de119-121">It then directs subsequent calls intended for that assembly to the backup copy.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de119-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="de119-122">See also</span></span>



[<span data-ttu-id="de119-123">KB 256946: vous recevez un message d'erreur de conflit de programmes lorsque vous démarrez Outlook 2000</span><span class="sxs-lookup"><span data-stu-id="de119-123">KB 256946: You receive a program conflict error message when you start Outlook 2000</span></span>](https://support.microsoft.com/kb/256946)
  
[<span data-ttu-id="de119-124">KB 228457: description de l'outil Fixmapi. exe inclus dans Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="de119-124">KB 228457: Description of the Fixmapi.exe Tool Included with Internet Explorer 5</span></span>](https://support.microsoft.com/kb/228457)

