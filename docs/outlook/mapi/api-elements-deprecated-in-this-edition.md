---
title: Éléments d’API déconseillées dans cette version
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: c70e89efba585183d2019bbda49102ecd14b9e20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782922"
---
# <a name="api-elements-deprecated-in-this-edition"></a>Éléments d’API déconseillées dans cette version

  
  
**S’applique à**: Outlook 
  
Éléments d’API suivants sont déconseillés dans Microsoft Outlook 2013. Ils ne sont plus pris en charge et vous ne devez pas les utiliser dans les nouveaux projets.
  
## <a name="deprecation-of-message-and-recipient-options"></a>Désapprobation de Message et des Options pour le destinataire

Éléments d’API suivants sont déconseillés dans cette version, en raison de message obsolète et les options pour le destinataire :
  
- **IXPLogon::RegisterOptions**: sous-système MAPI appelle n’est plus cette méthode pour établir des valeurs par défaut pour les options de message et le destinataire d’un fournisseur de transport.
    
- **OPTIONUTILITAIRE**— cette structure de données pris en charge des propriétés pour les options de message et le destinataire est obsolète. Le sous-système MAPI appelle n’est plus **IXPLogon::RegisterOptions** pour obtenir un message ou une option de destinataire prend en charge par un fournisseur de transport pour un type particulier. 
    
- **OPTIONCALLBACK**— ce prototype de la fonction, un fournisseur de transport utilisé pour déclarer une fonction de rappel et qui, à son tour, le sous-système MAPI utilisé pour résoudre les propriétés du fournisseur, est obsolète. Le sous-système MAPI n’est plus appelle **IXPLogon::RegisterOptions** ou utilise une fonction de rappel retournée par le fournisseur de transport. 
    
- **IMAPISession::MessageOptions**— les fournisseurs MAPI client et le service doivent appeler n’est plus de cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir les propriétés qui contrôlent un type particulier de message et l’adresse. La méthode renvoie toujours MAPI_E_NOT_FOUND, ce qui indique qu’il n’existe aucune option de message pour le message particulier.
    
- **IMAPISession::QueryDefaultMessageOpt**— les fournisseurs MAPI client et le service doivent appeler n’est plus de cette méthode pour récupérer les propriétés qui contrôlent les options de messages pour un type particulier. N’est plus, la méthode renvoie un pointeur vers un tableau de valeurs de propriété.
    
- **IAddrBook::RecipOptions**— les fournisseurs MAPI client et le service doivent appeler n’est plus de cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir les propriétés de contrôle du traitement d’un destinataire d’un type particulier. La méthode renvoie toujours MAPI_W_ERRORS_RETURNED, ce qui indique qu’il n’existe aucune option de destinataire pour le destinataire spécifique.
    
- **IAddrBook::QueryDefaultRecipOpt**— les fournisseurs MAPI client et le service doivent appeler n’est plus de cette méthode pour récupérer les propriétés qui contrôlent les options de destinataires pour un type particulier. N’est plus, la méthode renvoie un pointeur vers un tableau de valeurs de propriété.
    
## <a name="see-also"></a>Voir aussi



[Mise en route avec la r�f�rence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)

