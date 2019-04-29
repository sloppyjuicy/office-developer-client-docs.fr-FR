---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 53b2733dbf38d680027dc00ecf5513f384e46660
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417307"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Établit une session dans laquelle une application cliente se connecte à un fournisseur de transport. 
  
```cpp
HRESULT TransportLogon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG FAR * lpulFlags,
  LPMAPIERROR FAR * lppMAPIError,
  LPXPLOGON FAR * lppXPLogon
);
```

## <a name="parameters"></a>Paramètres

_lpMAPISup_: [in] pointeur vers l'objet de prise en charge du fournisseur de transport pour les fonctions de rappel au sein de MAPI pour cette session. Cet objet reste valide jusqu'à ce que le fournisseur de transport le libère.
    
_ulUIParam_: handle [in] vers la fenêtre parente des boîtes de dialogue ou des fenêtres que cette méthode affiche. Le paramètre _ulUIParam_ peut être non null, par exemple lorsque l'indicateur LOGON_SETUP est défini dans le paramètre _lpulFlags_ . 
    
_lpszProfileName_: pointeur vers le nom de profil de l'utilisateur. Le paramètre _lpszProfileName_ est principalement utilisé lorsqu'une boîte de dialogue doit être présentée. 
    
_lpulFlags_: [in, out] masque de des indicateurs qui contrôle la manière dont la session d'ouverture de session est établie. Les indicateurs suivants peuvent être définis lors de l'entrée par le spouleur MAPI:
    
  - LOGON_NO_CONNECT: le compte d'utilisateur se connecte à ce fournisseur de transport à des fins autres que la transmission et la réception des messages. Le fournisseur de transport ne doit pas essayer de se connecter à d'autres systèmes de messagerie.
        
  - LOGON_NO_DIALOG: aucune boîte de dialogue ne doit s'afficher même si les informations d'identification de l'utilisateur actuellement enregistrées ne sont pas valides ou sont insuffisantes pour l'ouverture de session.
        
  - LOGON_NO_INBOUND: le fournisseur de transport ne doit pas initialiser la réception des messages et ne doit pas accepter les messages entrants. Le spouleur MAPI peut utiliser la méthode [IXPLogon:: TransportNotify](ixplogon-transportnotify.md) ultérieurement pour signaler au fournisseur de transport d'activer le traitement des messages entrants. 
        
  - LOGON_NO_OUTBOUND: le fournisseur de transport ne doit pas initialiser pour l'envoi de messages, car le spouleur MAPI n'en fournit pas. Si une application cliente requiert une connexion à un fournisseur distant pendant la composition d'un message afin qu'elle puisse effectuer des appels de méthode [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) , le fournisseur de transport doit établir la connexion. Le spouleur MAPI peut utiliser **TransportNotify** pour signaler au fournisseur de transport quand les opérations sortantes peuvent commencer. 
      
  - MAPI_UNICODE: la chaîne passée pour le nom de profil est au format Unicode. Si l'indicateur\_Unicode Unicode n'est pas défini, la chaîne est au format ANSI.
      
    Les indicateurs suivants peuvent être définis sur sortie par le fournisseur de transport:
      
  - LOGON_SP_IDLE: demande que le spouleur MAPI appelle fréquemment la méthode [IXPLogon:: Idle](ixplogon-idle.md) du fournisseur de transport pour le traitement du temps d'inactivité. 
      
  - LOGON_SP_POLL: demande que le spouleur MAPI appelle fréquemment la méthode [IXPLogon::P oll](ixplogon-poll.md) sur l'objet d'ouverture de session renvoyé pour vérifier l'accès aux nouveaux messages. Si cet indicateur n'est pas défini, le spouleur MAPI vérifie uniquement les nouveaux messages lorsque le fournisseur de transport utilise la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) pour informer le spouleur qu'il y a de nouveaux messages à traiter. Un fournisseur de transport devient effectivement Send-only en ne définissant pas cet indicateur et en n'avertissant pas le spouleur MAPI de la réception des messages. 
      
  - LOGON_SP_RESOLVE: demande que le spouleur MAPI de la résolution complète adresse toutes les adresses de message pour les destinataires non pris en charge par ce fournisseur de transport. Par conséquent, le fournisseur de transport peut créer un chemin de réponse pour tous les destinataires.
      
  - MAPI_UNICODE: les chaînes renvoyées dans la structure [MAPIERROR](mapierror.md) , le cas échéant, sont au format Unicode. Si l'indicateur MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI. 
    
_lppMAPIError_: [out] pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée, le cas échéant, qui contient des informations de version, de composant et de contexte pour l'erreur. Le paramètre _lppMAPIError_ peut être défini sur null s'il n'existe aucune structure **MAPIERROR** à renvoyer. 
    
_lppXPLogon_: [out] pointeur vers le pointeur vers l'objet de connexion du fournisseur de transport renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK: l'appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_FAILONEPROVIDER: ce fournisseur ne peut pas se connecter, mais cette erreur ne doit pas désactiver le service. 
    
MAPI_E_UNCONFIGURED: le profil ne contient pas suffisamment d'informations pour que la connexion soit terminée. MAPI appelle la fonction de point d'entrée du service de messagerie du fournisseur.
    
MAPI_E_UNKNOWN_CPID: le fournisseur ne peut pas prendre en charge la page de code du client.
    
MAPI_E_UNKNOWN_LCID: le fournisseur ne peut pas prendre en charge les informations de paramètres régionaux du client.
    
MAPI_E_USER_CANCEL: l'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPProvider:: TransportLogon** pour établir une session d'ouverture de session pour un utilisateur. 
  
La plupart des fournisseurs de transport utilisent la méthode [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) fournie avec l'objet de prise en charge pointé par le paramètre _lpMAPISup_ pour l'enregistrement et la récupération des informations d'identité de l'utilisateur, des adresses de serveur et des informations d'identification. À l'aide de **OpenProfileSection**, un fournisseur de transport peut enregistrer des informations arbitraires et l'associer à une connexion à une ressource particulière. Par exemple, un fournisseur peut utiliser **OpenProfileSection** pour enregistrer le nom de compte et le mot de passe associés à une session particulière, ainsi que les noms de serveur ou d'autres informations nécessaires pour accéder aux ressources de cette session. MAPI masque les informations associées à une ressource provenant d'un accès externe. La section de profil mise à disposition via _lpMAPISup_ est gérée par le spouleur MAPI afin que les données associées à ce contexte utilisateur soient séparées des données pour d'autres contextes. 
  
Le fournisseur de transport doit appeler la méthode **IUnknown:: AddRef** sur l'objet support et conserver une copie du pointeur vers cet objet dans le cadre de l'objet de connexion du fournisseur. 
  
Le nom d'affichage du profil dans _lpszProfileName_ est fourni afin que le fournisseur de transport puisse l'utiliser dans les messages d'erreur ou les boîtes de dialogue d'ouverture de session. Si le fournisseur conserve ce nom, il doit être copié dans le stockage alloué par le fournisseur. 
  
Les fournisseurs de transport étroitement couplés avec d'autres fournisseurs de services peuvent avoir à effectuer des tâches supplémentaires à l'ouverture de session pour établir les bonnes informations d'identification requises pour les opérations entre les fournisseurs auxiliaires.
  
En règle générale, les fournisseurs de transport sont ouverts lorsque l'utilisateur se connecte pour la première fois à un profil. Étant donné que la première connexion à un profil est généralement assurée avant toute connexion à un magasin de messages, le spouleur MAPI appelle généralement **TransportLogon** avec les indicateurs LOGON_NO_INBOUND et LOGON_NO_OUTBOUND définis dans _lpulFlags_. Par la suite, lorsque les banques de messages appropriées sont disponibles dans la session de profil, le spouleur MAPI appelle **TransportNotify** pour lancer des opérations entrantes et sortantes pour le fournisseur de transport. 
  
Le passage de l'indicateur LOGON_NO_CONNECT dans _lpulFlags_ signale le fonctionnement hors connexion du fournisseur de transport. Cet indicateur indique qu'aucune connexion externe ne doit être établie; Si le fournisseur de transport ne peut pas établir de session sans connexion externe, il doit renvoyer une valeur d'erreur pour la connexion. 
  
Un fournisseur de transport doit définir l'indicateur LOGON_SP_IDLE dans _lpulFlags_ au moment de l'initialisation s'il est conçu pour utiliser le temps pendant lequel le système passe inactif. Ce délai est souvent utilisé pour gérer les opérations automatiques, telles que le téléchargement automatique de messages, le téléchargement de messages minutés ou l'envoi de messages chronométrés. Si cet indicateur est défini, le spouleur MAPI **** appelle inactif lorsque le temps d'inactivité du système se produit pour lancer ces opérations. Le spouleur MAPI n'appelle **** pas inactif à des intervalles définis; au lieu de cela, il est appelé uniquement pendant une durée d'inactivité réelle. Par conséquent, les fournisseurs ne doivent pas traiter de l'hypothèse de **** la fréquence à laquelle leurs méthodes inactives seront appelées. Les fournisseurs qui prennent en charge les opérations de temps d'inactivité doivent fournir une interface utilisateur de configuration pour lui dans la feuille de propriétés du fournisseur. 
  
Si la connexion du fournisseur de transport réussit, le fournisseur doit renvoyer dans le paramètre _lppXPLogon_ un pointeur vers un objet Logon. Le spouleur MAPI utilise cet objet pour un accès fournisseur supplémentaire. Si **TransportLogon** affiche une boîte de dialogue d'ouverture de session et que l'utilisateur annule l'ouverture de session en cliquant sur le bouton **Annuler** dans la boîte de dialogue, le fournisseur doit renvoyer MAPI_E_USER_CANCEL. 
  
Pour la plupart des valeurs d'erreur renvoyées par **TransportLogon**, MAPI désactive les services de messagerie auxquels le fournisseur appartient. MAPI n'appelle pas de fournisseurs appartenant à ce service pour le reste de la session MAPI. En revanche, lorsque **TransportLogon** renvoie la valeur d'erreur MAPI_E_FAILONEPROVIDER à partir de son ouverture de session, MAPI ne désactive pas le service de messagerie auquel appartient le fournisseur. **TransportLogon** doit renvoyer MAPI_E_FAILONEPROVIDER s'il rencontre une erreur qui ne garantit pas la désactivation du service pour le reste de la session. 
  
Si un fournisseur renvoie MAPI_E_UNCONFIGURED à partir de son ouverture de session, MAPI appelle la fonction d'entrée de service de message du fournisseur, puis tente à nouveau d'ouvrir une session. MAPI transmet MSG_SERVICE_CONFIGURE comme contexte, afin de permettre au service de se configurer lui-même. Si le client a choisi d'autoriser une interface utilisateur sur la connexion, le service peut présenter sa feuille de propriétés de configuration pour permettre à l'utilisateur d'entrer des informations de configuration. 
  
Si le fournisseur constate que toutes les informations requises ne se trouvent pas dans le profil, il doit renvoyer MAPI_E_UNCONFIGURED afin que MAPI appelle la fonction de point d'entrée du service de messagerie du fournisseur. 
  
## <a name="see-also"></a>Voir aussi

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

