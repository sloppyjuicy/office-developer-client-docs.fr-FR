---
title: Profils MAPI
description: Les profils MAPI sont divisés en sections auxquelles les clients et les fournisseurs de services accèdent pour afficher les propriétés de profil aux utilisateurs ou pour apporter des modifications de configuration.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 493c87a4-317d-47ec-850b-342cac59594b
ms.openlocfilehash: 903bd810f670382d6a8e2c60f2130c8e255e7207
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65811801"
---
# <a name="mapi-profiles"></a>Profils MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un profil stocke des informations sur les fournisseurs de services et les services de messages installés sur un ordinateur. Pour chaque session, un client au moment de la connexion sélectionne un profil qui décrit les fournisseurs et services à utiliser. Un client peut choisir parmi une collection de profils et, si vous le souhaitez, en établir un par défaut. Le profil par défaut est le profil qui est sélectionné automatiquement lorsqu’un client démarre une session et n’a pas spécifié explicitement de profil.
  
Également dans ces rubriques, vous trouverez une discussion sur le cache de surnom, qui est stocké dans un flux binaire.
  
- [Cache de surnoms](nickname-cache.md)
    
- [Flux de saisie semi-automatique](autocomplete-stream.md)
    
- [Analyse de fichiers binaires](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Sections de profil

Les profils sont divisés en sections auxquelles les clients et les fournisseurs de services accèdent pour afficher les propriétés de profil aux utilisateurs ou pour apporter des modifications de configuration. Une section de profil est un objet MAPI qui implémente l’interface **IProfSect** , une interface qui dérive **d’IMAPIProp** et n’a aucune méthode supplémentaire. Pour plus d’informations, consultez [IProfSect : IMAPIProp](iprofsectimapiprop.md). Son seul objectif est de manipuler les propriétés d’une section de profil. Pour récupérer un pointeur **IProfSect** vers une section de profil particulière, les clients et les fournisseurs de services appellent les méthodes suivantes. 
  
|Propriété |Valeur |
|:-----|:-----|
|Les clients peuvent appeler :  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Les fournisseurs de services peuvent appeler :  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Les clients ou fournisseurs peuvent appeler :  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Les profils sont organisés hiérarchiquement de la même façon que MAPISVC. Fichier INF. En haut de la hiérarchie, il existe des sections de profil qui contiennent des informations pertinentes pour le profil. Le niveau intermédiaire comprend des sections qui contiennent des informations sur un service de message particulier et le niveau inférieur inclut des sections qui contiennent des informations sur l’un des fournisseurs de services dans un service de message. 
  
Chaque profil a plusieurs propriétés requises qui sont stockées dans une ou plusieurs sections du profil. Par exemple, chaque profil a les propriétés **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). La clé de recherche d’un profil est définie sur la valeur définie dans MAPIGUID. H comme MUID_PROFILE_INSTANCE et est toujours garanti d’être unique parmi tous les profils. Bien que deux profils puissent avoir le même nom, ils ne peuvent pas avoir la même clé de recherche. Les clés de recherche doivent être traitées comme des données binaires au lieu de données de n’importe quel type particulier.
  
Les fournisseurs de magasins de messages doivent inclure la propriété **PR_DISPLAY_NAME** de leur magasin de messages ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans les sections de profil du profil et de leur fournisseur de magasin de messages, et pour maintenir la synchronisation de ces entrées. Lorsqu’un magasin de messages est créé, le fournisseur définit **PR_DISPLAY_NAME** en fonction de la valeur stockée dans ces sections de profil. 
  
Il existe deux différences majeures entre les sections de profil et les autres objets qui héritent **d’IMAPIProp** : 
  
- Les sections de profil ne prennent pas en charge les transactions.
    
- Les sections de profil ne prennent pas en charge les propriétés nommées, en retournant MAPI_E_NO_SUPPORT à partir de leurs **implémentations IMAPIProp::GetIDsFromNames** et **IMAPIProp::GetNamesFromIDs** . Pour plus d’informations, consultez [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Étant donné que les sections de profil ne prennent pas en charge les transactions, les modifications apportées avec les appels à **IMAPIProp::CopyProps**, **CopyTo** ou **SetProps prennent** immédiatement effet. Pour plus d’informations, consultez [IMAPIProp::CopyProps](imapiprop-copyprops.md). Les clients et les fournisseurs de services peuvent appeler la méthode **IMAPIProp::SaveChanges** d’une section de profil et elle réussit, mais elle n’affecte pas les données de la section de profil. Pour plus d’informations, consultez [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Des modifications immédiates peuvent affecter la façon dont les fournisseurs de services implémentent les feuilles de propriétés que les clients utilisent pour afficher les propriétés de profil aux utilisateurs. Les fournisseurs de services qui souhaitent que les utilisateurs puissent reporter ou annuler des modifications doivent implémenter leurs feuilles de propriétés avec des copies des sections de profil au lieu des sections réelles. En utilisant des copies, les utilisateurs peuvent apporter des modifications, puis annuler ultérieurement ces modifications, en laissant les sections de profil d’origine intactes. 
  
L’ordre dans lequel les informations apparaissent dans un profil affecte la façon dont MAPI configure les ressources et effectue des affectations dans une session. Les affectations suivantes sont affectées par l’ordre de profil :
  
- Magasin de messages par défaut
    
- Carnet d’adresses personnel
    
- Chemin de recherche du magasin de messages par défaut
    
- Chemin de recherche du carnet d’adresses par défaut
    
- Ordre du fournisseur de transport
    
MAPI définit le magasin de messages par défaut comme le premier magasin de messages dans le profil dont l’indicateur STATUS_DEFAULT_STORE est défini dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)), ce qui indique qu’il peut s’agir du magasin par défaut. Les clients peuvent remplacer ce paramètre en appelant **IMAPISession::SetDefaultStore**. Pour plus d’informations, consultez [IMAPISession::SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI crée un ordre de transport pour la gestion des messages sortants et entrants. Lorsque plusieurs fournisseurs de transport se sont inscrits pour un message d’un type particulier, MAPI utilise cet ordre pour déterminer quel fournisseur doit gérer le message. MAPI définit l’ordre de transport comme l’ordre dans lequel les fournisseurs de transport ont été ajoutés au profil à une exception près : les transports qui définissent l’indicateur STATUS_XP_PREFER_LAST dans leur propriété **PR_RESOURCE_FLAGS** sont positionnés en dernier dans l’ordre. Les clients peuvent définir l’ordre de transport en appelant **IMsgServiceAdmin::MsgServiceTransportOrder**. Pour plus d’informations, consultez [IMsgServiceAdmin::MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Ces instructions relatives à l’ordre des fournisseurs de services et des services de messages peuvent parfois entrer en conflit. En cas de conflit, votre code doit résoudre le conflit. Vous pouvez utiliser le programme Courrier Panneau de configuration pour inspecter un profil que vous avez créé pour déterminer si les fournisseurs ont été configurés comme prévu.
  

