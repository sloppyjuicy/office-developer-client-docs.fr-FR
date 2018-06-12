---
title: Ouvrir le carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4b9d7b8cf71b4e00dac6022e1dda727ef7a23036
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784930"
---
# <a name="opening-the-address-book"></a><span data-ttu-id="aa992-103">Ouvrir le carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="aa992-103">Opening the address book</span></span>

<span data-ttu-id="aa992-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa992-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa992-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span><span class="sxs-lookup"><span data-stu-id="aa992-p101">Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile.</span></span> 
  
<span data-ttu-id="aa992-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span><span class="sxs-lookup"><span data-stu-id="aa992-p102">**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning.</span></span> 
  
<span data-ttu-id="aa992-p103">Les clients non interactives doivent ignorer l'avertissement et poursuit comme si la m�thode a r�ussi. L'interface renvoy�e **IAddrBook** n'est valide que si toutes, certaines ou aucune des fournisseurs de carnet d'adresses dans le profil sont en cours d'ex�cution. Par cons�quent, � la fois interactives et les clients doivent toujours n'oubliez pas de lib�rer le pointeur **IAddrBook** lors de la fin de la session.</span><span class="sxs-lookup"><span data-stu-id="aa992-p103">Noninteractive clients should ignore the warning and proceed as if the method succeeded. The returned **IAddrBook** interface is valid regardless of whether all, some, or none of the address book providers in the profile are running. Therefore, both interactive and noninteractive clients must always remember to release the **IAddrBook** pointer when the session ends.</span></span> 
  

