---
title: IXPProviderTransportLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPProvider.TransportLogon
api_type:
- COM
ms.assetid: 534929f2-36a2-463d-8c4c-d86060cde127
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 89a2cc10d7ee7e177c8dcbbbd28e89a26656b7e6
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62461974"
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

_lpMAPISup_ : [in] Pointeur vers l’objet de support du fournisseur de transport pour les fonctions de rappel dans MAPI pour cette session. Cet objet reste valide jusqu’à ce que le fournisseur de transport le relâche.
    
_ulUIParam_: [in] Handle to the parent window of any dialog boxes or windows this method displays. Le  _paramètre ulUIParam_ peut être non null, par exemple lorsque l’indicateur LOGON_SETUP est définie dans _le paramètre lpulFlags_ . 
    
_lpszProfileName_: [in] Pointeur vers le nom de profil de l’utilisateur. Le  _paramètre lpszProfileName_ est principalement utilisé lorsqu’une boîte de dialogue doit être présentée. 
    
_lpulFlags_: [in, out] Masque de bits d’indicateurs qui contrôle la façon dont la session d’ouverture de session est établie. Les indicateurs suivants peuvent être définies lors de l’entrée par lepooler MAPI :
    
  - LOGON_NO_CONNECT : le compte d’utilisateur se connecte à ce fournisseur de transport à des fins autres que la transmission et la réception des messages. Le fournisseur de transport ne doit pas tenter d’établir de connexions avec d’autres systèmes de messagerie.
        
  - LOGON_NO_DIALOG : aucune boîte de dialogue ne doit s’afficher même si les informations d’identification de l’utilisateur actuellement enregistrées ne sont pas valides ou insuffisantes pour la connexion.
        
  - LOGON_NO_INBOUND : le fournisseur de transport n’a pas à s’initialiser pour la réception des messages et ne doit pas accepter les messages entrants. Lepooler MAPI peut utiliser la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) ultérieurement pour indiquer au fournisseur de transport d’activer le traitement des messages entrants. 
        
  - LOGON_NO_OUTBOUND : le fournisseur de transport n’a pas à s’initialiser pour l’envoi de messages, car lepooler MAPI n’en fournit aucun. Si une application cliente nécessite une connexion à un fournisseur distant pendant la composition d’un message afin de pouvoir effectuer des appels de méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , le fournisseur de transport doit établir la connexion. Lepooler MAPI peut utiliser **TransportNotify** pour signaler au fournisseur de transport que les opérations sortantes peuvent commencer. 
      
  - MAPI_UNICODE : la chaîne transmise pour le nom de profil est au format Unicode. Si l’indicateur MAPIUNICODE\_ n’est pas définie, la chaîne est au format ANSI.
      
    Les indicateurs suivants peuvent être définies sur la sortie par le fournisseur de transport :
      
  - LOGON_SP_IDLE : demande aupooler MAPI d’appeler fréquemment la méthode [IXPLogon::Idle](ixplogon-idle.md) du fournisseur de transport pour le traitement des périodes d’inactivité. 
      
  - LOGON_SP_POLL : demande aupooler MAPI d’appeler fréquemment la méthode [IXPLogon::P élément](ixplogon-poll.md) sur l’objet d’enregistrement renvoyé pour vérifier la création de nouveaux messages. Si cet indicateur n’est pas définie, lepooler MAPI vérifie uniquement les nouveaux messages lorsque le fournisseur de transport utilise la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) pour informer lepooler qu’il y a de nouveaux messages à traiter. Un fournisseur de transport devient en réalité un fournisseur d’envoi uniquement en ne fixant pas cet indicateur et en notifiant lepooler MAPI de la réception du message. 
      
  - LOGON_SP_RESOLVE : demande que lepooler MAPI résolve en adresses complètes toutes les adresses de message pour les destinataires non pris en charge par ce fournisseur de transport. Par conséquent, le fournisseur de transport peut construire un chemin de réponse pour tous les destinataires.
      
  - MAPI_UNICODE : les chaînes renvoyées dans la structure [MAPIERROR](mapierror.md) , le caser, sont au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
_lppMAPIError_ : [out] Pointeur vers un pointeur vers la structure **MAPIERROR** renvoyée, le cas cas, qui contient les informations de version, de composant et de contexte de l’erreur. Le  _paramètre lppMAPIError_ peut avoir la valeur NULL s’il n’existe aucune structure **MAPIERROR** à renvoyer. 
    
_lppXPLogon_ : [out] Pointeur vers le pointeur vers l’objet d’logon du fournisseur de transport renvoyé.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK : l’appel a réussi et a renvoyé la ou les valeurs attendues.
    
MAPI_E_FAILONEPROVIDER : ce fournisseur ne peut pas se connecter, mais cette erreur ne doit pas désactiver le service. 
    
MAPI_E_UNCONFIGURED : le profil ne contient pas suffisamment d’informations pour que la logon soit terminée. MAPI appelle la fonction de point d’entrée du service de messagerie du fournisseur.
    
MAPI_E_UNKNOWN_CPID : le fournisseur ne peut pas la prise en charge de la page de code du client.
    
MAPI_E_UNKNOWN_LCID : le fournisseur ne peut pas la prise en charge des informations de paramètres régionaux du client.
    
MAPI_E_USER_CANCEL : l’utilisateur a annulé l’opération, généralement en cliquant sur le **bouton Annuler dans** une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Lepooler MAPI appelle la méthode **IXPProvider::TransportLogon** pour établir une session d’ouverture de session pour un utilisateur. 
  
La plupart des fournisseurs de transport utilisent la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) fournie avec l’objet de support pointé par le paramètre  _lpMAPISup_ pour enregistrer et récupérer les informations d’identité utilisateur, les adresses serveur et les informations d’identification. À **l’aide d’OpenProfileSection**, un fournisseur de transport peut enregistrer des informations arbitraires et les associer à une ouverture de conférence à une ressource particulière. Par exemple, un fournisseur peut utiliser **OpenProfileSection** pour enregistrer le nom de compte et le mot de passe associés à une session particulière, ainsi que les noms de serveur ou autres informations nécessaires nécessaires pour accéder aux ressources de cette session. MAPI masque les informations associées à une ressource de l’accès externe. La section de profil rendue disponible via  _lpMAPISup_ est gérée par lepooler MAPI de sorte que les données liées à ce contexte utilisateur sont séparées des données pour d’autres contextes. 
  
Le fournisseur de transport doit appeler la méthode **IUnknown::AddRef** sur l’objet de support et conserver une copie du pointeur vers cet objet dans le cadre de l’objet d’accès fournisseur. 
  
Le nom d’affichage du  _profil dans lpszProfileName_ est fourni afin que le fournisseur de transport puisse l’utiliser dans les messages d’erreur ou les boîtes de dialogue d’accès. Si le fournisseur conserve ce nom, il doit être copié dans le stockage alloué par le fournisseur. 
  
Les fournisseurs de transport qui sont étroitement associés à d’autres fournisseurs de services peuvent avoir à faire des opérations supplémentaires lors de l’connexion afin d’établir les bonnes informations d’identification requises pour les opérations entre les fournisseurs complémentaires.
  
En règle générale, les fournisseurs de transport sont ouverts lorsque l’utilisateur se connecte pour la première fois à un profil. Étant donné que la première ouverture de page d’un profil intervient généralement avant l’ouverture de une boutique de messages, lepooler MAPI appelle généralement **TransportLogon** avec les indicateurs LOGON_NO_INBOUND et LOGON_NO_OUTBOUND définies dans  _les indicateurs lpulFlags_. Plus tard, lorsque les magasins de messages appropriés sont disponibles dans la session de profil, lepooler MAPI appelle **TransportNotify** pour lancer les opérations entrantes et sortantes pour le fournisseur de transport. 
  
Transmission de l LOGON_NO_CONNECT dans  _les lpulFlags_ signale le fonctionnement hors connexion du fournisseur de transport. Cet indicateur indique qu’aucune connexion externe ne doit être réalisée . Si le fournisseur de transport ne peut pas établir une session sans connexion externe, il doit renvoyer une valeur d’erreur pour l’ouverture de session. 
  
Un fournisseur de transport doit définir l’indicateur LOGON_SP_IDLE dans  _les lpulFlags_ au moment de l’initialisation s’il est conçu pour utiliser le temps d’inactivité du système. Cette durée est souvent utilisée pour gérer les opérations automatiques, telles que le téléchargement automatique des messages, le téléchargement de messages timed ou l’envoi de messages timed. Si cet indicateur est définie, lepooler MAPI appelle **Idle** lorsque la durée d’inactivité du système se produit pour lancer de telles opérations. Lepooler MAPI n’appelle pas **Inactif** à intervalles définis ; Au lieu de cela, il est appelé uniquement pendant les périodes d’inactivité réelles. Par conséquent, les fournisseurs ne doivent pas travailler sur une hypothèse sur la fréquence d’appel de leurs méthodes **Idle** . Les fournisseurs qui prendre en charge les opérations de temps d’inactivité doivent fournir une interface utilisateur de configuration pour celle-ci dans leur feuille de propriétés de fournisseur. 
  
Si l’logo du fournisseur de transport réussit, le fournisseur doit renvoyer dans le paramètre _lppXPLogon_ un pointeur vers un objet d’logon. Lepooler MAPI utilisera cet objet pour un accès fournisseur supplémentaire. Si **TransportLogon** affiche une boîte de dialogue d’accès et que l’utilisateur annule généralement l’accès en  cliquant sur le bouton Annuler dans la boîte de dialogue, le fournisseur doit MAPI_E_USER_CANCEL. 
  
Pour la plupart des valeurs d’erreur **renvoyées par TransportLogon**, MAPI désactive les services de messagerie à laquelle le fournisseur appartient. MAPI n’appellera aucun fournisseur qui appartient à ce service pour le reste de la session MAPI. En revanche, lorsque **TransportLogon** renvoie la valeur d’erreur MAPI_E_FAILONEPROVIDER à partir de son logo, MAPI ne désactive pas le service de messagerie auquel appartient le fournisseur. **TransportLogon** doit renvoyer MAPI_E_FAILONEPROVIDER si elle rencontre une erreur qui ne justifie pas la désactivation du service pour le reste de la session. 
  
Si un fournisseur renvoie MAPI_E_UNCONFIGURED à partir de sa logon, MAPI appelle la fonction d’entrée de service de messagerie du fournisseur, puis réessaye d’y revenir. MAPI passe MSG_SERVICE_CONFIGURE comme contexte, pour donner au service la possibilité de se configurer lui-même. Si le client a choisi d’autoriser une interface utilisateur sur la logon, le service peut présenter sa feuille de propriétés de configuration afin que l’utilisateur puisse entrer des informations de configuration. 
  
Si le fournisseur trouve que toutes les informations requises ne se trouvent pas dans le profil, il doit renvoyer MAPI_E_UNCONFIGURED afin que MAPI appelle la fonction de point d’entrée du service de messagerie du fournisseur. 
  
## <a name="see-also"></a>Voir aussi

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

