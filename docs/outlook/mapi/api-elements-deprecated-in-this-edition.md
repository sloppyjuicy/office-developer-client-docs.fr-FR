---
title: Éléments d'API déConseillés dans cette édition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d0a6d182-961c-4496-a3bd-f643612527a5
description: 'Derni�re modification�: lundi 25 juin 2012'
ms.openlocfilehash: abfe734ad8af436f52fc0308d0cd236078bb47df
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318206"
---
# <a name="api-elements-deprecated-in-this-edition"></a>Éléments d'API déConseillés dans cette édition

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les éléments d'API suivants sont déconseillés dans Microsoft Outlook 2013. Elles ne sont plus prises en charge et vous ne devez pas les utiliser dans de nouveaux projets.
  
## <a name="deprecation-of-message-and-recipient-options"></a>DésApprobation des options de message et de destinataire

Les éléments d'API suivants sont déconseillés dans cette version en raison des options de message et de destinataire obsolètes:
  
- **IXPLogon:: RegisterOptions**— le sous-système MAPI n'appelle plus cette méthode pour établir des valeurs par défaut pour les options de message et de destinataire d'un fournisseur de transport.
    
- **** La structure de données qui prend en charge les propriétés des options de message et de destinataire est obsolète. Le sous-système MAPI n'appelle plus **IXPLogon:: RegisterOptions** pour obtenir les options de message ou de destinataire prises en charge par un fournisseur de transport pour un type d'adresse particulier. 
    
- **OPTIONCALLBACK**: ce prototype de fonction, qu'un fournisseur de transport a utilisé pour déclarer une fonction de rappel et qui, à son tour, le sous-système MAPI utilisé pour résoudre les propriétés du fournisseur, est obsolète. Le sous-système MAPI n'appelle plus **IXPLogon:: RegisterOptions** ou utilise une fonction de rappel renvoyée par le fournisseur de transport. 
    
- **IMAPISession:: MessageOptions**: les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir des propriétés qui contrôlent un message et un type d'adresse spécifiques. La méthode renvoie toujours MAPI_E_NOT_FOUND, ce qui indique qu'il n'y a pas d'options de message pour le message en particulier.
    
- **IMAPISession:: QueryDefaultMessageOpt**— les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour récupérer les propriétés qui contrôlent les options de message pour un type d'adresse particulier. La méthode ne renvoie plus un pointeur vers un tableau de valeurs de propriété.
    
- **IAddrBook:: RecipOptions**: les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour afficher les propriétés ou permettre aux utilisateurs de définir des propriétés qui contrôlent le traitement pour un destinataire d'un type d'adresse particulier. La méthode renvoie toujours MAPI_W_ERRORS_RETURNED, ce qui indique qu'il n'y a pas d'options de destinataire pour le destinataire particulier.
    
- **IAddrBook:: QueryDefaultRecipOpt**— les fournisseurs de services et clients MAPI ne doivent plus appeler cette méthode pour récupérer les propriétés qui contrôlent les options de destinataire pour un type d'adresse particulier. La méthode ne renvoie plus un pointeur vers un tableau de valeurs de propriété.
    
## <a name="see-also"></a>Voir aussi



[Mise en route avec la référence de MAPI pour Outlook 2013](getting-started-with-the-outlook-mapi-reference.md)

