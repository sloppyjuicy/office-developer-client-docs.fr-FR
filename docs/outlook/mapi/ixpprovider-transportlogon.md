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
ms.openlocfilehash: 96e81442125ae49e0c2856a1cf3a97a16d3453cf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583336"
---
# <a name="ixpprovidertransportlogon"></a>IXPProvider::TransportLogon

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Établit une session dans lequel une application cliente se connecte à un fournisseur de transport. 
  
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

_lpMAPISup_: [in] pointeur vers l’objet de prise en charge du fournisseur de transport pour les fonctions de rappel dans MAPI pour cette session. Cet objet reste valide jusqu'à ce que le fournisseur de transport le libère.
    
_ulUIParam_: [Handle vers la fenêtre parente de toutes les boîtes de dialogue ou windows cette méthode affiche in]. Le paramètre _ulUIParam_ peut être non null, par exemple, lorsque la LOGON_SETUP indicateur est définie dans le paramètre _lpulFlags_ . 
    
_lpszProfileName_: [in] pointeur vers le nom du profil de l’utilisateur. Le paramètre _lpszProfileName_ est principalement utilisé lorsqu’une boîte de dialogue doit être présentée. 
    
_lpulFlags_: [dans, out] masque de bits d’indicateurs qui contrôle la façon dont l’ouverture de session est établie. Les indicateurs suivants peuvent être définis à l’entrée par le spouleur MAPI :
    
  - LOGON_NO_CONNECT : Le compte d’utilisateur se connecte à ce fournisseur de transport à des fins autres que l’émission et la réception de messages. Le fournisseur de transport ne doit pas essayer établir des connexions à d’autres systèmes de messagerie.
        
  - LOGON_NO_DIALOG : Aucune boîte de dialogue ne doit être affiché même si les informations d’identification de l’utilisateur actuellement enregistrés sont non valides ou insuffisants pour l’ouverture de session.
        
  - LOGON_NO_INBOUND : Le fournisseur de transport n’a pas d’initialisation pour la réception de messages et ne doit pas accepter les messages entrants. Le spouleur MAPI peut utiliser la méthode [IXPLogon::TransportNotify](ixplogon-transportnotify.md) ultérieurement pour signaler le fournisseur de transport pour activer le traitement des messages entrants. 
        
  - LOGON_NO_OUTBOUND : Le fournisseur de transport ne dispose pas d’initialiser l’envoi des messages, comme le spouleur MAPI ne fournit aucune. Si une application cliente requiert une connexion à un fournisseur distant pendant la composition d’un message afin qu’il puisse faire des appels de méthode [IXPLogon::AddressTypes](ixplogon-addresstypes.md) , le fournisseur de transport doit établir la connexion. Le spouleur MAPI permet de signaler le fournisseur de transport lors d’opérations sortantes peuvent commencer **TransportNotify** . 
      
  - MAPI_UNICODE : La chaîne transmise pour le nom de profil est au format Unicode. Si l’interface MAPI\_indicateur UNICODE n’est pas définie, la chaîne est au format ANSI.
      
    Indicateurs ci-dessous peuvent être définies sur sortie par le fournisseur de transport :
      
  - LOGON_SP_IDLE : Demandes que le spouleur MAPI appelle fréquemment méthode de [IXPLogon::Idle](ixplogon-idle.md) du fournisseur de transport pour le traitement des périodes d’inactivité. 
      
  - LOGON_SP_POLL : Demandes le spouleur MAPI fréquemment appeler la méthode [IXPLogon::Poll](ixplogon-poll.md) sur l’objet retourné d’ouverture de session pour vérifier les nouveaux messages. Si cet indicateur n’est pas défini, le spouleur MAPI vérifie uniquement pour les nouveaux messages lorsque le fournisseur de transport utilise la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) pour notifier le spouleur qu’il existe des nouveaux messages à traiter. Un fournisseur de transport devient envoyer uniquement en définissant ne pas cet indicateur et en avertir ne pas le spouleur MAPI de la réception du message. 
      
  - LOGON_SP_RESOLVE : Les demandes de résoudre le spouleur MAPI total des adresses de toutes les adresses de message pour des destinataires non pris en charge par ce fournisseur de transport. Par conséquent, que le fournisseur de transport pouvez construire un chemin d’accès de réponse pour tous les destinataires.
      
  - MAPI_UNICODE : Les chaînes retournées dans la structure [MAPIERROR](mapierror.md) , le cas échéant, sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI. 
    
_lppMAPIError_: [out] pointeur vers un pointeur vers la structure **MAPIERROR** retournée, le cas échéant, qui contient des informations de version, composant et le contexte de l’erreur. Le paramètre _lppMAPIError_ peut être défini sur la valeur NULL s’il n’existe aucune structure **MAPIERROR** pour renvoyer. 
    
_lppXPLogon_: [out] pointeur vers le pointeur vers l’objet d’ouverture de session du fournisseur de transport renvoyée.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK : L’appel a réussi et a renvoyé la valeur attendue ou les valeurs.
    
Référence à MAPI_E_FAILONEPROVIDER : Ce fournisseur ne peut pas se connecter, mais cette erreur ne doit pas désactiver le service. 
    
MAPI_E_UNCONFIGURED : Le profil ne contient pas de suffisamment d’informations pour l’ouverture de session à effectuer. MAPI appelle la fonction de point d’entrée du service de message du fournisseur.
    
MAPI_E_UNKNOWN_CPID : Le fournisseur ne peut pas en charge de page de codes du client.
    
MAPI_E_UNKNOWN_LCID : Le fournisseur ne peut pas prendre en charge les informations de paramètres régionaux du client.
    
MAPI_E_USER_CANCEL : L’utilisateur a annulé l’opération, en général en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
## <a name="remarks"></a>Remarques

Le spouleur MAPI appelle la méthode **IXPProvider::TransportLogon** pour établir une ouverture de session pour un utilisateur. 
  
La plupart des fournisseurs de transport utiliser la méthode [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) fournie avec l’objet de prise en charge désigné par le paramètre _lpMAPISup_ pour l’enregistrement et la récupération des informations d’identité utilisateur, les adresses de serveur et les informations d’identification. À l’aide de **OpenProfileSection**, un fournisseur de transport peut enregistrer des informations arbitraires et l’associer à une connexion à une ressource particulière. Par exemple, un fournisseur peut utiliser **OpenProfileSection** pour enregistrer le nom de compte et mot de passe associé à une session particulière et les noms de serveur ou autres informations nécessaires sont nécessaires pour accéder aux ressources pour cette session. MAPI masque les informations associées à une ressource à partir de l’accès externe. La section profil rendue disponible par le biais de _lpMAPISup_ est gérée par le spouleur MAPI afin que les données liées à ce contexte utilisateur sont séparées à partir des données d’autres contextes. 
  
Le fournisseur de transport doit appeler la méthode **IUnknown::AddRef** sur l’objet de prise en charge et conserver une copie du pointeur à cet objet dans le cadre de l’objet de connexion du fournisseur. 
  
Le nom complet de profil dans _lpszProfileName_ est fourni pour que le fournisseur de transport puisse l’utiliser dans les boîtes de dialogue d’ouverture de session ou les messages d’erreur. Si le fournisseur conserve ce nom, il doit être copié vers un stockage alloué par le fournisseur. 
  
Fournisseurs de transport qui sont étroitement liés à d’autres fournisseurs de services peuvent être nécessaire de travail supplémentaire à l’ouverture de session pour établir les informations d’identification d’une bonne requises pour les opérations entre les fournisseurs de Compagnon.
  
En règle générale, les fournisseurs de transport sont ouverts lorsque l’utilisateur tout d’abord se connecte à un profil. Étant donné que la première connexion à un profil donc généralement vient avant ouverture de session dans le magasin de message, le spouleur MAPI appelle généralement **TransportLogon** avec les indicateurs LOGON_NO_OUTBOUND et LOGON_NO_INBOUND définis dans _lpulFlags_. Plus tard, lorsque les banques de messages appropriés sont disponibles dans la session de profil, le spouleur MAPI appelle **TransportNotify** pour lancer des opérations pour le fournisseur de transport entrantes et sortantes. 
  
En transmettant l’indicateur LOGON_NO_CONNECT dans des signaux _lpulFlags_ opération en mode hors connexion du fournisseur de transport. Cet indicateur signale qu'aucuns les connexions externes ne doivent être faites ; Si le fournisseur de transport ne peuvent pas établir une session sans une connexion externe, il doit renvoyer une valeur d’erreur pour l’ouverture de session. 
  
Un fournisseur de transport doit définir l’indicateur LOGON_SP_IDLE de _lpulFlags_ lors de l’initialisation si elle est conçue pour utiliser le temps passé par le système dans le cas contraire inactif. Ce temps est souvent utilisé pour gérer les opérations automatiques, telle qu’automatique des messages le téléchargement, délai de téléchargement du message ou le délai de dépôt des messages. Si cet indicateur est défini, le spouleur MAPI appelle **inactif** lors de la durée d’inactivité système d’initier des opérations. Le spouleur MAPI n’appelle pas **inactif** à intervalles réguliers ; au lieu de cela, elle est appelée uniquement pendant la durée d’inactivité true. Par conséquent, les fournisseurs ne doivent pas fonctionner sur n’importe quel hypothèse sur la fréquence à laquelle seront appelées leurs méthodes **inactif** . Les fournisseurs qui prennent en charge les opérations de périodes d’inactivité doivent fournir une interface utilisateur de configuration pour qu’il dans leur feuille de propriétés du fournisseur. 
  
Si la connexion au fournisseur du transport aboutit, le fournisseur doit retourner dans le paramètre _lppXPLogon_ un pointeur vers un objet d’ouverture de session. Le spouleur MAPI utilise cet objet pour l’accès fournisseur supplémentaires. Si **TransportLogon** affiche une boîte de dialogue d’ouverture de session et l’utilisateur annule généralement d’ouverture de session en cliquant sur le bouton **Annuler** dans la boîte de dialogue le fournisseur doit retourner MAPI_E_USER_CANCEL. 
  
La plupart des valeurs d’erreur renvoyé à partir de **TransportLogon**, MAPI désactive les services de messagerie à laquelle appartient le fournisseur. MAPI ne sera pas appeler tous les fournisseurs qui appartiennent à ce service pour le reste de la session MAPI. En revanche, **TransportLogon** retourne la valeur d’erreur de référence à MAPI_E_FAILONEPROVIDER à partir de son ouverture de session MAPI ne désactive pas le service de message à laquelle appartient le fournisseur. **TransportLogon** doit renvoyer la référence à MAPI_E_FAILONEPROVIDER si elle rencontre une erreur qui ne garantit pas la désactivation du service pour le reste de la session. 
  
Si un fournisseur renvoie MAPI_E_UNCONFIGURED à partir de son ouverture de session, MAPI sont alors appeler la fonction de l’entrée de service de message du fournisseur et recommencez l’ouverture de session. MAPI passe MSG_SERVICE_CONFIGURE comme le contexte, pour donner à un risque de se configurer le service. Si le client a choisi d’autoriser une interface utilisateur à l’ouverture de session, le service peut représenter sa feuille de propriétés de configuration afin que l’utilisateur peut entrer des informations de configuration. 
  
Si le fournisseur qui recherche toutes les informations requises ne sont pas dans le profil, elle doit retourner MAPI_E_UNCONFIGURED afin que MAPI appelle la fonction de point d’entrée du service de message du fournisseur. 
  
## <a name="see-also"></a>Voir aussi

- [IXPProvider : IUnknown](ixpprovideriunknown.md)  
- [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)  
- [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md)  
- [IXPLogon::AddressTypes](ixplogon-addresstypes.md)  
- [IXPLogon::Idle](ixplogon-idle.md)  
- [IXPLogon::Poll](ixplogon-poll.md)  
- [IXPLogon::TransportNotify](ixplogon-transportnotify.md) 
- [MAPIERROR](mapierror.md)

