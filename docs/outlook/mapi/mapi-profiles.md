---
title: Profils MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 7f241fde8aedeae9debc66f728ee21c1c6bed6fb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784663"
---
# <a name="mapi-profiles"></a>Profils MAPI

  
  
**S’applique à**: Outlook 
  
Un profil stocke des informations sur les fournisseurs de services et les services de messagerie qui sont installés sur un ordinateur. Pour chaque session, un client au moment de l’ouverture de session sélectionne un seul profil qui décrit les fournisseurs et les services à utiliser. Un client peut choisir d’une collection de profils et, si vous le souhaitez, établir un en tant que la valeur par défaut. Le profil par défaut est le profil qui est sélectionné automatiquement lorsqu’un client démarre une session et un profil n’a pas explicitement spécifié.
  
Dans ces rubriques, vous trouverez également une discussion sur le cache du surnom, qui est stocké dans un objet stream binaire.
  
- [Cache du surnom dans](nickname-cache.md)
    
- [Flux de saisie semi-automatique](autocomplete-stream.md)
    
- [L’analyse des fichiers binaires](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Sections de profil

Profils sont divisées en sections que les clients et fournisseurs de services accéder pour afficher les propriétés de profil pour les utilisateurs ou pour apporter des modifications de configuration. Une section de profil est un objet MAPI qui implémente l’interface **IProfSect** , une interface qui dérive de **IMAPIProp** et possède pas de méthodes supplémentaires. Pour plus d’informations, voir [IProfSect : IMAPIProp](iprofsectimapiprop.md). Son seul but est pour manipuler les propriétés d’une section de profil. Pour récupérer un pointeur **IProfSect** à une section de profil particulier, clients et fournisseurs de services appeler les méthodes suivantes. 
  
|||
|:-----|:-----|
|Les clients peuvent appeler :  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Fournisseurs de services peuvent appeler :  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Clients ou fournisseurs peuvent appeler :  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Profils sont organisées de façon hiérarchique beaucoup comme le fichier MAPISVC.inf. Fichier. En haut de la hiérarchie, il existe des sections de profil qui contiennent des informations relatives au profil. Le niveau intermédiaire comporte des sections qui contiennent des informations sur un service particulier de message et le niveau inférieur comporte des sections qui contiennent des informations sur un des fournisseurs de services dans un service de message. 
  
Chaque profil possède plusieurs propriétés requises qui sont stockées dans un ou plusieurs des sections du profil. Par exemple, chaque profil a les **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) et les propriétés de **clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). Clé de recherche d’un profil est définie sur la valeur définie dans MAPIGUID. H en tant que MUID_PROFILE_INSTANCE et est toujours unique parmi tous les profils. Bien que deux profils peuvent avoir le même nom, ils ne peuvent pas avoir la même clé de recherche. Clés de recherche doivent être traitées en tant que données binaires plutôt que des données d’un type particulier.
  
Fournisseurs de magasins de message sont requis pour inclure leur propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) du message dans les sections de profil pour le profil et pour leur message fournisseur de magasins et de garder ces entrées synchronisées. Lors de la création d’une banque de messages, le fournisseur définit **PR_DISPLAY_NAME** en fonction de la valeur stockée dans ces sections du profil. 
  
Il existe deux principales différences entre les sections de profil et d’autres objets qui héritent de **IMAPIProp**: 
  
- Sections profil ne prennent pas en charge transactions.
    
- Sections profil n’acceptent pas les propriétés nommées, renvoi MAPI_E_NO_SUPPORT à partir de leurs implémentations **IMAPIProp::GetIDsFromNames** et **IMAPIProp::GetNamesFromIDs** . Pour plus d’informations, voir [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Étant donné que les sections de profil ne prennent pas en charge les transactions, toutes les modifications apportées par des appels à **IMAPIProp::CopyProps**, **CopyTo**ou **SetProps** immédiatement prennent effet. Pour plus d’informations, voir [IMAPIProp::CopyProps](imapiprop-copyprops.md). Clients et fournisseurs de services peuvent appeler la méthode de **IMAPIProp::SaveChanges** d’une section de profil et réussit, mais elle n’affecte pas les données de la section profil. Pour plus d’informations, voir [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Avoir des modifications se produisent immédiatement peut affecter les comment les fournisseurs de services implémentent les feuilles de propriétés que les clients utilisent pour afficher les propriétés de profil aux utilisateurs. Fournisseurs de services que vous souhaitez que les utilisateurs puissent différer ou annuler les modifications doivent implémenter leurs feuilles de propriété avec les copies des sections de profil au lieu des sections réelles. À l’aide de copies, les utilisateurs peuvent apporter des modifications et puis ultérieurement Annuler les modifications, en laissant les sections de profil d’origine intacts. 
  
L’ordre dans lequel les informations apparaissent dans un profil affecte comment MAPI configure les ressources et effectue des affectations dans une session. Les affectations suivantes sont affectées par ordre de profil :
  
- Banque de messages par défaut
    
- Carnet d’adresses personnel
    
- Chemin de recherche de magasin de message par défaut
    
- Chemin de recherche de livre adresse par défaut
    
- Ordre des fournisseurs de transport
    
MAPI définit la banque de messages par défaut à la première banque de messages dans le profil de l’indicateur STATUS_DEFAULT_STORE dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)), ce qui indique qu’il peut être la banque par défaut. Les clients peuvent remplacer ce paramètre en appelant **IMAPISession::SetDefaultStore**. Pour plus d’informations, voir [IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI crée un ordre de transport pour la gestion des messages entrants et sortants. Lorsque plusieurs fournisseurs de transport a inscrit pour un message d’un type particulier, MAPI utilise cette commande pour déterminer le fournisseur doit traiter le message. MAPI définit l’ordre de transport à l’ordre dans lequel le transport fournisseurs ont été ajoutés au profil à une seule exception : les transports de définir l’indicateur STATUS_XP_PREFER_LAST dans leur propriété **PR_RESOURCE_FLAGS** sont positionnés en dernier dans l’ordre. Les clients peuvent définir l’ordre de transport en appelant **IMsgServiceAdmin::MsgServiceTransportOrder**. Pour plus d’informations, voir [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Ces instructions pour le classement des fournisseurs de services et les services de messagerie peuvent parfois entrer en conflit. S’il existe un conflit, votre code doit résoudre le conflit. Vous pouvez utiliser le programme de messagerie le panneau de configuration pour inspecter un profil que vous avez créée pour déterminer si les fournisseurs ont été configurés comme prévu.
  

