---
title: Ouverture du carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 79e0bc93-f37d-4f6a-beed-7519d01e0056
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6d1a7e8e1d9debd7eb715bbe4958657c000f1e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326165"
---
# <a name="opening-the-address-book"></a>Ouverture du carnet d’adresses

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Call [IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) to open the integrated address book and retrieve a pointer to the MAPI [IAddrBook : IMAPIProp](iaddrbookimapiprop.md) interface. The methods of the **IAddrBook** interface can be used to access entries in all of the containers of each of the address book providers in the profile. 
  
**OpenAddressBook** might return a warning, MAPI_W_ERRORS_RETURNED, to indicate that there were problems with one or more of the address book providers. Interactive clients should call [IMAPISession::GetLastError](imapisession-getlasterror.md) to retrieve additional error information and display the returned information the first time they call **OpenAddressBook** and it returns a warning. 
  
Les clients non interactives doivent ignorer l'avertissement et poursuit comme si la m�thode a r�ussi. L'interface renvoy�e **IAddrBook** n'est valide que si toutes, certaines ou aucune des fournisseurs de carnet d'adresses dans le profil sont en cours d'ex�cution. Par cons�quent, � la fois interactives et les clients doivent toujours n'oubliez pas de lib�rer le pointeur **IAddrBook** lors de la fin de la session. 
  

