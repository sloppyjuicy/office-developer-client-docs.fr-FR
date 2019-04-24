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
ms.openlocfilehash: 9db1f8e163e44a44df1e798cebccb3639325275e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340081"
---
# <a name="mapi-profiles"></a>Profils MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un profil stocke des informations sur les fournisseurs de services et les services de messagerie installés sur un ordinateur. Pour chaque session, un client au moment de la connexion sélectionne un profil qui décrit les fournisseurs et les services à utiliser. Un client peut choisir parmi une collection de profils et, si vous le souhaitez, en établir un comme valeur par défaut. Le profil par défaut est le profil qui est sélectionné automatiquement lorsqu'un client démarre une session et n'a pas explicitement spécifié de profil.
  
Dans ces rubriques, vous trouverez également une description du cache des surnoms, qui est stocké dans un flux binaire.
  
- [Cache de surnoms](nickname-cache.md)
    
- [Flux de saisie semi-automatique](autocomplete-stream.md)
    
- [Analyse de fichiers binaires](https://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
    
## <a name="profile-sections"></a>Sections de profil

Les profils sont divisés en sections auxquelles les clients et fournisseurs de services accèdent pour afficher les propriétés de profil pour les utilisateurs ou pour modifier la configuration. Une section de profil est un objet MAPI qui implémente l'interface **IProfSect** , une interface qui dérive de **IMAPIProp** et n'a pas de méthodes supplémentaires. Pour plus d'informations, voir [IProfSect: IMAPIProp](iprofsectimapiprop.md). Son seul objectif est de manipuler les propriétés d'une section de profil. Pour récupérer un pointeur **IProfSect** vers une section de profil particulière, les clients et les fournisseurs de services appellent les méthodes suivantes. 
  
|||
|:-----|:-----|
|Les clients peuvent appeler:  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Les fournisseurs de services peuvent appeler:  <br/> |[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) <br/> |
|Les clients ou fournisseurs peuvent appeler les éléments suivants:  <br/> |[IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) <br/> |
   
Les profils sont organisés de manière hiérarchique comme le MAPISVC. Fichier INF. En haut de la hiérarchie, il existe des sections de profil qui contiennent des informations relatives au profil. Le niveau intermédiaire inclut des sections qui contiennent des informations sur un service de messagerie particulier et le niveau inférieur inclut des sections qui contiennent des informations sur l'un des fournisseurs de services dans un service de messagerie. 
  
Chaque profil dispose de plusieurs propriétés requises qui sont stockées dans une ou plusieurs sections du profil. Par exemple, chaque profil a les propriétés **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)) et **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). La clé de recherche d'un profil est définie sur la valeur définie dans MAPIGUID. H en tant que MUID_PROFILE_INSTANCE et est toujours unique pour tous les profils. Bien que deux profils puissent avoir le même nom, ils ne peuvent pas avoir la même clé de recherche. Les clés de recherche doivent être considérées comme des données binaires au lieu de données de n'importe quel type particulier.
  
Les fournisseurs de banques de messages doivent inclure la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) de leur banque de messages dans les sections de profil pour le profil et pour leur fournisseur de banque de messages, et pour conserver ces entrées synchronisées. Lorsqu'une banque de messages est créée, le fournisseur définit **PR_DISPLAY_NAME** en fonction de la valeur stockée dans ces sections de profil. 
  
Il existe deux différences majeures entre les sections de profil et les autres objets qui héritent de **IMAPIProp**: 
  
- Les sections de profil ne prennent pas en charge les transactions.
    
- Les sections de profil ne prennent pas en charge les propriétés nommées, en retournant MAPI_E_NO_SUPPORT à partir de leurs implémentations **IMAPIProp:: GetIDsFromNames** et **IMAPIProp:: GetNamesFromIDs** . Pour plus d'informations, voir [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) et [IMAPIProp:: GetNamesFromIDs](imapiprop-getnamesfromids.md).
    
Étant donné que les sections de profil ne prennent pas en charge les transactions, les modifications apportées avec des appels à **IMAPIProp:: CopyProps**, **CopyTo**ou **SetProps** prennent immédiatement effet. Pour plus d'informations, voir [IMAPIProp:: CopyProps](imapiprop-copyprops.md). Les clients et fournisseurs de services peuvent appeler la méthode **IMAPIProp:: SaveChanges** d'une section de profil et cela réussit, mais il n'affecte pas les données de la section de profil. Pour plus d'informations, voir [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). Les modifications apportées immédiatement peuvent influer sur la façon dont les fournisseurs de services implémentent les feuilles de propriétés utilisées par les clients pour afficher les propriétés de profil aux utilisateurs. Les fournisseurs de services qui souhaitent que les utilisateurs puissent ajourner ou annuler des modifications doivent implémenter leurs feuilles de propriétés avec des copies de sections de profil au lieu des sections réelles. En utilisant des copies, les utilisateurs peuvent faire des modifications, puis annuler ces modifications, sans toucher aux sections du profil d'origine. 
  
L'ordre dans lequel les informations s'affichent dans un profil affecte la façon dont MAPI configure les ressources et crée des affectations dans une session. Les affectations suivantes sont affectées par l'ordre des profils:
  
- Banque de messages par défaut
    
- Carnet d'adresses personnel
    
- Chemin de recherche par défaut de la Banque de messages
    
- Chemin de recherche par défaut du carnet d'adresses
    
- Ordre des fournisseurs de transport
    
MAPI définit la Banque de messages par défaut comme étant la première banque de messages du profil dont l'indicateur STATUS_DEFAULT_STORE est défini dans sa propriété **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)), ce qui indique qu'il peut s'agir de la Banque par défaut. Les clients peuvent remplacer ce paramètre en appelant **IMAPISession:: SetDefaultStore**. Pour plus d'informations, voir [IMAPISession:: SetDefaultStore](imapisession-setdefaultstore.md).
  
MAPI crée un ordre de transport pour gérer les messages sortants et entrants. Lorsque plusieurs fournisseurs de transport ont été inscrits pour un message d'un type particulier, MAPI utilise cette commande pour déterminer le fournisseur qui doit gérer le message. MAPI définit l'ordre de transport sur l'ordre dans lequel les fournisseurs de transport ont été ajoutés au profil à l'aide d'une exception: les transports qui définissent l'indicateur STATUS_XP_PREFER_LAST dans leur propriété **PR_RESOURCE_FLAGS** sont positionnés en dernier dans l'ordre. Les clients peuvent définir l'ordre de transport en appelant **IMsgServiceAdmin:: MsgServiceTransportOrder**. Pour plus d'informations, voir [IMsgServiceAdmin:: MsgServiceTransportOrder](imsgserviceadmin-msgservicetransportorder.md).
  
Ces instructions relatives à la classification des services de messagerie et des fournisseurs de services peuvent parfois être en conflit. En cas de conflit, votre code doit résoudre le conflit. Vous pouvez utiliser le programme panneau de configuration de messagerie pour inspecter un profil que vous avez créé afin de déterminer si les fournisseurs ont été configurés comme prévu.
  

