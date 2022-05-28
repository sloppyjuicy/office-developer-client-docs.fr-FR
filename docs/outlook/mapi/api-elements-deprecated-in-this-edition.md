---
title: Éléments d’API déconseillés dans cette édition
description: Décrit les éléments d’API qui ne sont plus pris en charge et ne doivent pas être utilisés dans Microsoft Outlook 2013.
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
ms.openlocfilehash: 6135a38072f2733199dc2f066634ec3372aa3be7
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65770438"
---
# <a name="api-elements-deprecated-in-this-edition"></a>Éléments d’API déconseillés dans cette édition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les éléments d’API suivants sont déconseillés dans Microsoft Outlook 2013. Elles ne sont plus prises en charge et vous ne devez pas les utiliser dans de nouveaux projets.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Dépréciation des options message et destinataire

Les éléments d’API suivants sont déconseillés dans cette version en raison des options de message et de destinataire obsolètes :
  
- **IXPLogon::RegisterOptions** : le sous-système MAPI n’appelle plus cette méthode pour établir les valeurs par défaut des options de message et de destinataire pour un fournisseur de transport.
    
- **OPTIONDATA** : cette structure de données qui prenait en charge les propriétés pour les options de message et de destinataire est obsolète. Le sous-système MAPI n’appelle plus **IXPLogon::RegisterOptions** pour obtenir les options de message ou de destinataire prises en charge par un fournisseur de transport pour un type d’adresse particulier. 
    
- **OPTIONCALLBACK** : ce prototype de fonction, qu’un fournisseur de transport a utilisé pour déclarer une fonction de rappel et qui, à son tour, le sous-système MAPI utilisé pour résoudre les propriétés du fournisseur, est obsolète. Le sous-système MAPI n’appelle plus **IXPLogon::RegisterOptions** ou n’utilise aucune fonction de rappel retournée par le fournisseur de transport. 
    
- **IMAPISession::MessageOptions** : les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir des propriétés qui contrôlent un message et un type d’adresse particuliers. La méthode retourne toujours MAPI_E_NOT_FOUND, ce qui indique qu’il n’existe aucune option de message pour le message particulier.
    
- **IMAPISession::QueryDefaultMessageOpt** : les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour récupérer les propriétés qui contrôlent les options de message pour un type d’adresse particulier. La méthode ne retourne plus de pointeur vers un tableau de valeurs de propriété.
    
- **IAddrBook::RecipOptions** : les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir des propriétés qui contrôlent le traitement d’un destinataire d’un type d’adresse particulier. La méthode retourne toujours MAPI_W_ERRORS_RETURNED, ce qui indique qu’il n’existe aucune option de destinataire pour le destinataire particulier.
    
- **IAddrBook::QueryDefaultRecipOpt** : les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour récupérer les propriétés qui contrôlent les options de destinataire pour un type d’adresse particulier. La méthode ne retourne plus de pointeur vers un tableau de valeurs de propriété.
    
## <a name="see-also"></a>Voir aussi



[Mise en route avec la référence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)

