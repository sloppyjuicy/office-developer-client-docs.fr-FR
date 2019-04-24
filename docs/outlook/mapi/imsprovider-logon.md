---
title: IMSProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Logon
api_type:
- COM
ms.assetid: 890d9cbe-3570-4cf0-aeae-667c0e5ba181
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 9c7f62c69c7a06f7ca0e4bfddcf789cddc536ea6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309666"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Journalise MAPI sur une instance d'un fournisseur de banque de messages.
  
```cpp
HRESULT Logon(
  LPMAPISUP lpMAPISup,
  ULONG_PTR ulUIParam,
  LPSTR lpszProfileName,
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  ULONG ulFlags,
  LPCIID lpInterface,
  ULONG FAR * lpcbSpoolSecurity,
  LPBYTE FAR * lppbSpoolSecurity,
  LPMAPIERROR FAR * lppMAPIError,
  LPMSLOGON FAR * lppMSLogon,
  LPMDB FAR * lppMDB
);
```

## <a name="parameters"></a>Paramètres

 _lpMAPISup_
  
> dans Pointeur vers l'objet de prise en charge MAPI actuel pour la Banque de messages.
    
 _ulUIParam_
  
> dans Handle de la fenêtre parente de toutes les boîtes de dialogue ou fenêtres que cette méthode affiche. 
    
 _lpszProfileName_
  
> dans Pointeur vers une chaîne qui contient le nom du profil utilisé pour la connexion du fournisseur de banque. Cette chaîne peut être affichée dans les boîtes de dialogue, écrites dans un fichier journal ou simplement ignorée. Elle doit être au format Unicode si l'indicateur MAPI_UNICODE est défini dans le paramètre _ulFlags_ . 
    
 _cbEntryID_
  
> dans Taille, en octets, de l'identificateur d'entrée pointé par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> dans Pointeur vers l'identificateur d'entrée pour la Banque de messages. Le fait de transmettre **null** dans _lpEntryID_ indique qu'une banque de messages n'a pas encore été sélectionnée et que les boîtes de dialogue permettant à l'utilisateur de sélectionner une banque de messages peuvent être présentées. 
    
 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le mode d'exécution de l'ouverture de session. Les indicateurs suivants peuvent être définis:
    
MAPI_DEFERRED_ERRORS 
  
> L'appel est autorisé même si l'objet sous-jacent n'est pas disponible pour l'implémentation de l'appel. Si l'objet n'est pas disponible, un appel ultérieur à l'objet peut déclencher une erreur.
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si MAPI_UNICODE n'est pas défini, les chaînes sont au format ANSI.
    
MDB_NO_DIALOG 
  
> Empêche l'affichage des boîtes de dialogue d'ouverture de session. Si cet indicateur est défini, la valeur d'erreur MAPI_E_LOGON_FAILED est renvoyée si l'ouverture de session échoue. Si cet indicateur n'est pas défini, le fournisseur de banque de messages peut demander à l'utilisateur de corriger un nom ou un mot de passe, d'insérer un disque ou d'effectuer d'autres actions nécessaires pour établir une connexion avec le magasin.
    
MDB_NO_MAIL 
  
> La Banque de messages ne doit pas être utilisée pour l'envoi ou la réception de messages. L'indicateur signale à MAPI de ne pas avertir le spouleur MAPI que cette banque de messages est en cours d'ouverture. Si cet indicateur est défini et que la Banque de messages est étroitement couplée avec un fournisseur de transport, le fournisseur n'a pas besoin d'appeler la méthode [IMAPISupport:: SpoolerNotify](imapisupport-spoolernotify.md) . 
    
MDB_TEMPORARY 
  
> Ouvre une session sur la Banque afin que les informations puissent être récupérées par programme à partir de la section profil, sans utiliser de boîtes de dialogue. Cet indicateur indique à MAPI que la Banque ne doit pas être ajoutée à la table de banque de messages et que le magasin ne peut pas être rendu permanent. Si cet indicateur est défini, les fournisseurs de banques de messages n'ont pas besoin d'appeler la méthode [IMAPISupport:: ModifyProfile](imapisupport-modifyprofile.md) . 
    
MDB_WRITE 
  
> Demande une autorisation en lecture/écriture.
    
 _lpInterface_
  
> dans Pointeur vers l'identificateur d'interface (IID) pour la Banque de messages à laquelle se connecter. La transmission de la **valeur null** indique que l'interface MAPI pour la Banque de messages ( [IMsgStore](imsgstoreimapiprop.md)) est renvoyée. Le paramètre _lpInterface_ peut également être défini sur un identificateur pour une interface appropriée pour la Banque de messages (par exemple, IID_IUnknown ou IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> remarquer Pointeur vers la variable dans laquelle le fournisseur de banque d'informations renvoie la taille, en octets, des données de validation dans le paramètre _lppbSpoolSecurity_ . 
    
 _lppbSpoolSecurity_
  
> remarquer Pointeur vers le pointeur vers les données de validation renvoyées. Ces données de validation sont fournies afin que la méthode [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md) puisse enregistrer le spouleur MAPI sur le même magasin que le fournisseur de banque de messages. 
    
 _lppMAPIError_
  
> remarquer Pointeur vers un pointeur vers la structure [MAPIERROR](mapierror.md) renvoyée, le cas échéant, qui contient des informations de version, de composant et de contexte pour une erreur. Le paramètre _lppMAPIError_ peut être défini sur **null** s'il n'existe aucune structure **MAPIERROR** à renvoyer. 
    
 _lppMSLogon_
  
> remarquer Pointeur vers le pointeur vers l'objet d'ouverture de session de la Banque de messages pour que MAPI ouvre une session.
    
 _lppMDB_
  
> remarquer Pointeur vers le pointeur vers l'objet de la Banque de messages pour le spouleur MAPI et les applications clientes auxquelles se connecter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_FAILONEPROVIDER 
  
> Ce fournisseur ne peut pas se connecter, mais cette erreur ne doit pas désactiver le service. 
    
MAPI_E_LOGON_FAILED 
  
> Une session de connexion n'a pas pu être établie.
    
MAPI_E_UNCONFIGURED 
  
> Le profil ne contient pas suffisamment d'informations pour que la connexion soit terminée. Lorsque cette valeur est renvoyée, MAPI appelle la fonction de point d'entrée de service de message du fournisseur de banque de messages.
    
MAPI_E_USER_CANCEL 
  
> L'utilisateur a annulé l'opération, généralement en cliquant sur le bouton **Annuler** d'une boîte de dialogue. 
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n'est pas configuré pour prendre en charge la page de code du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n'est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_W_ERRORS_RETURNED 
  
> L'appel a réussi, mais le fournisseur de banque de messages contient des informations d'erreur disponibles. Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md). Pour obtenir les informations d'erreur du fournisseur, appelez la méthode [IMAPISession:: GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **IMSProvider:: Logon** pour effectuer la majorité du traitement nécessaire pour obtenir l'accès à une banque de messages. Les fournisseurs de banque de messages valident toutes les informations d'identification utilisateur nécessaires pour accéder à une banque particulière et renvoient un objet de banque de messages dans le paramètre _lppMDB_ que le spouleur MAPI et les applications clientes peuvent ouvrir. 
  
En plus de l'objet de banque de messages renvoyé pour l'utilisation par le client et le spouleur MAPI, le fournisseur renvoie également un objet d'ouverture de session de banque de messages que MAPI doit utiliser pour contrôler le magasin ouvert. L'objet d'ouverture de session de la Banque de messages et l'objet de banque de messages doivent être étroitement liés dans le fournisseur de banque de messages pour que chacun d'eux puisse affecter l'autre. L'utilisation de l'objet Store et de l'objet Logon doit être identique; il doit y avoir une correspondance un-à-un entre l'objet d'ouverture de session et l'objet Store de sorte que les objets agissent comme s'il s'agissait d'un objet qui expose deux interfaces. Les deux objets doivent également être créés et libérés ensemble. 
  
L'objet de prise en charge MAPI, créé par MAPI et transmis au fournisseur dans le paramètre _lpMAPISup_ , permet d'accéder aux fonctions de MAPI requises par le fournisseur. Il s'agit notamment des fonctions qui enregistrent et extraient les informations de profil, les carnets d'adresses Access, etc. Le pointeur _lpMAPISup_ peut être différent pour chaque banque ouverte. Lors du traitement des appels pour une banque de messages après l'ouverture de session, le fournisseur de banque d'informations doit utiliser la variable _lpMAPISup_ propre à cette banque. Pour tout appel **d'ouverture de session** qui ouvre une banque de messages et réussit lors de la création d'un objet d'ouverture de session de la Banque de messages, le fournisseur doit enregistrer un pointeur vers l'objet de prise en charge MAPI dans l'objet de connexion Store et doit appeler la méthode [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour ajouter une référence pour objet support. 
  
Le paramètre _ulUIParam_ doit être utilisé si le fournisseur présente des boîtes de dialogue lors de l'appel de **connexion** . Toutefois, les boîtes de dialogue ne doivent pas être présentées si _ulFlags_ contient l'indicateur MDB_NO_DIALOG. Si une interface utilisateur doit être appelée mais que _ulFlags_ ne l'autorise pas ou si, pour une raison quelconque, une interface utilisateur ne peut pas être affichée, le fournisseur doit renvoyer MAPI_E_LOGON_FAILED. Si l' **ouverture de session** affiche une boîte de dialogue et que l'utilisateur annule l'ouverture de session, généralement en cliquant sur le bouton **Annuler** de la boîte de dialogue, le fournisseur doit renvoyer MAPI_E_USER_CANCEL. 
  
Le paramètre _lpEntryID_ peut être **null** ou pointer vers un identificateur d'entrée de magasin non encapsulé que cette banque de messages a précédemment créée. Si _lpEntryID_ pointe vers un identificateur d'entrée déenveloppée, cet identificateur d'entrée peut provenir de l'un des emplacements suivants: 
  
- Il peut s'agir d'un identificateur d'entrée que le fournisseur de banque a précédemment encapsulé et écrit dans la section de profil sous la forme d'une propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Il peut s'agir d'un identificateur d'entrée que le fournisseur a précédemment encapsulé et renvoyé à un client appelant sous la forme d'une propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Il peut s'agir d'un identificateur d'entrée que le fournisseur a précédemment encapsulé et renvoyé à un client appelant en tant que propriété **PR_ENTRYID** d'un objet de banque de messages. 
    
Dans l'un de ces cas, il est possible que l'identificateur d'entrée ait été créé sur un autre ordinateur que celui actuellement utilisé.
  
Lorsque _lpEntryID_ n'est pas **null**, il doit contenir toutes les informations nécessaires pour identifier et localiser la Banque de messages. Ces informations peuvent inclure les noms de volume réseau, les numéros de téléphone, les noms de compte d'utilisateur, etc. Si la connexion au magasin ne peut pas être établie à l'aide des données de l'identificateur d'entrée, le fournisseur de banque d'informations doit afficher une boîte de dialogue qui permet à l'utilisateur de sélectionner le magasin à ouvrir. Une boîte de dialogue peut être requise, par exemple, si un serveur a été renommé, si un nom de compte a été modifié ou si des parties du réseau ne sont pas disponibles.
  
Lorsque _lpEntryID_ est **null**, la Banque de messages à utiliser n'a pas encore été sélectionnée. Le fournisseur peut toujours accéder à un magasin sans afficher de boîte de dialogue s'il prend en charge des méthodes supplémentaires pour spécifier le magasin. Par exemple, le fournisseur peut vérifier son fichier d'initialisation, ou il peut rechercher des propriétés supplémentaires qui ont été placées dans sa section de profil du service de messagerie au niveau de la configuration.
  
Si un fournisseur constate que toutes les informations requises ne se trouvent pas dans le profil, il doit renvoyer MAPI_E_UNCONFIGURED. MAPI appellera ensuite la fonction de point d'entrée du service de messagerie du fournisseur pour permettre à l'utilisateur de sélectionner un magasin, ou même d'en créer un, et d'entrer un nom de compte et un mot de passe, selon les besoins. MAPI crée automatiquement une nouvelle section de profil pour une nouvelle banque; Cette nouvelle section de profil peut être temporaire ou permanente, en fonction de la façon dont elle a été ajoutée. Si le fournisseur de Banque appelle la méthode **IMAPISupport:: ModifyProfile** , la section nouveau profil devient permanente et la Banque est ajoutée à la liste des magasins de messages renvoyée par la méthode [IMAPISession:: GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Le paramètre _lpInterface_ spécifie l'IID de l'interface requise pour l'objet Store récemment ouvert. Le fait de transmettre **null** dans _lpInterface_ spécifie que l'interface de banque de messages MAPI, **IMsgStore**, est requise. Le fait de transmettre l'objet de banque de messages, IID_IMsgStore, spécifie également que **IMsgStore** est requis. Si IID_IUnknown est transmis dans _lpInterface_, le fournisseur doit ouvrir le magasin à l'aide de l'interface dérivée de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) qui convient le mieux pour le fournisseur (il s'agit généralement de **IMsgStore**). Lorsque IID_IUnknown est transmis, l'implémentation de l'appel utilise la méthode [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) pour sélectionner une interface après la réussite de l'opération Store Open. 
  
L'appel de **IMSProvider:: Logon** doit renvoyer des informations suffisantes, telles qu'un chemin d'accès à la Banque et des informations d'identification pour accéder au magasin, afin de permettre au spouleur MAPI de se connecter au même magasin que le fournisseur de banque sans présenter de boîte de dialogue. Les paramètres _lpcbSpoolSecurity_ et _lppbSpoolSecurity_ sont utilisés pour renvoyer ces informations. Le fournisseur alloue la mémoire pour ces données en passant un pointeur vers une mémoire tampon dans le paramètre _lpfAllocateBuffer_ de la fonction [MSProviderInit](msproviderinit.md) ; le fournisseur place la taille de cette mémoire tampon dans _lpcbSpoolSecurity_. 
  
MAPI libère cette mémoire tampon lorsque cela est nécessaire. Si la connexion du spouleur MAPI au magasin peut être accomplie à partir des informations contenues dans la section du profil, le fournisseur peut renvoyer la valeur null dans _lppbSpoolSecurity_ et 0 pour la taille des informations dans _lpcbSpoolSecurity_. L'ouverture de session du spouleur MAPI est effectuée dans le cadre d'un processus différent de celui de la connexion au magasin. étant donné que la mémoire tampon qui contient les informations transmises est copiée entre les processus, il se peut qu'elle ne soit pas en mémoire au même emplacement pour le processus de spouleur MAPI que pour le processus du fournisseur de banque. Par conséquent, un fournisseur ne doit pas placer d'adresses dans cette mémoire tampon. Pour plus d'informations sur la connexion du spouleur MAPI, voir la méthode [IMSProvider:: SpoolerLogon](imsprovider-spoolerlogon.md) . 
  
La plupart des fournisseurs de magasins utilisent la méthode [IMAPISession:: OpenProfileSection](imapisession-openprofilesection.md) de l'objet de prise en charge transmis dans le paramètre _lpMAPISup_ pour l'enregistrement et la récupération des informations d'identification et des options de l'utilisateur. **OpenProfileSection** permet à un fournisseur de banque d'informations d'enregistrer des informations arbitraires supplémentaires dans une section de profil et de l'associer à une ressource particulière. Par exemple, un fournisseur de banque d'informations peut enregistrer le nom de compte d'utilisateur et le mot de passe associés à une ressource, ainsi que les chemins d'accès ou autres informations nécessaires pour accéder à cette ressource. 
  
Les propriétés avec des identificateurs de propriété 0x6600 à 0x67FF sont des propriétés sécurisées disponibles pour le fournisseur pour sa propre utilisation afin de stocker des données privées dans des sections de profil. Pour plus d'informations sur les utilisations des propriétés dans les objets de section de profil, voir la méthode [IProfSect: IMAPIProp](iprofsectimapiprop.md) . 
  
En plus des données privées dans les propriétés avec des identificateurs 0x6600 à 0x67FF, le fournisseur de banque d'informations doit fournir des informations pour la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans sa section de profil. Il doit placer **PR_DISPLAY_NAME** le nom d'affichage du fournisseur lui-même, une chaîne d'identification (par exemple, «Banque d'informations personnelles Microsoft») qui est affichée aux utilisateurs afin qu'ils puissent distinguer cette banque de messages des autres auxquels ils peuvent avoir accès À. **PR_DISPLAY_NAME** contient généralement un nom de serveur, un nom de compte d'utilisateur ou un chemin d'accès. 
  
Certaines propriétés de section de profil sont visibles dans la table de banque de messages; d'autres sont visibles lors de l'installation, de l'installation et de la configuration du sous-système MAPI. En règle générale, le fournisseur fournit des informations pour ces propriétés visibles pour une nouvelle section de profil, qui n'inclut pas encore d'informations d'identification enregistrées ou d'informations confidentielles, et lorsqu'il trouve que les informations de propriété ont changé. Pour plus d'informations sur les sections de profil, voir [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md).
  
Après avoir réussi à se connecter à un utilisateur, et avant de revenir à MAPI, le fournisseur de banque d'information doit créer le tableau de propriétés pour la ligne d'état de la ressource et appeler la méthode [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) . 
  
 Les appels de **connexion** qui ouvrent des banques de messages qui sont déjà ouverts pour la session MAPI actuelle ignorent la majeure partie du traitement décrit précédemment. Ces appels ne créent pas de lignes d'État, renvoient les objets d'ouverture de session de magasin de messages, appellent **AddRef** pour l'objet de prise en charge MAPI ou renvoient des données pour la connexion du spouleur MAPI. Ces appels renvoient S_OK et renvoient un objet de banque de messages avec l'interface demandée. 
  
Pour détecter ces appels, le fournisseur doit gérer une liste dans l'objet fournisseur de banque de messages des magasins déjà ouverts pour cet objet fournisseur. Lors du traitement d'un appel **d'ouverture de session** , le fournisseur doit analyser cette liste de magasins ouverts et déterminer si le magasin auquel il doit se connecter est déjà ouvert. Si c'est le cas, les informations d'identification de l'utilisateur n'ont pas besoin d'être vérifiées et l'affichage d'une boîte de dialogue doit être évité, si possible. Si des boîtes de dialogue doivent être affichées, le fournisseur doit vérifier les informations renvoyées pour déterminer si un magasin a été ouvert une deuxième fois. De plus, le fournisseur doit vérifier les ouvertures en double à l'aide de _lpEntryID_ au début du traitement des appels **d'ouverture de session** . 
  
Le traitement standard pour un appel de **connexion** qui accède à une banque ouverte est le suivant: 
  
1. Le fournisseur Store appelle **AddRef** pour l'objet Store existant si la nouvelle interface demandée est identique à l'interface de la Banque existante. Dans le cas contraire, il appelle **QueryInterface** pour obtenir la nouvelle interface. Si la Banque ne prend pas en charge la nouvelle interface, le fournisseur doit renvoyer la valeur d'erreur MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Le fournisseur renvoie un pointeur vers l'interface requise de l'objet Store existant dans _lppMDB_.
    
3. Le fournisseur renvoie **null** dans _lppMSLogon_.
    
4. Le fournisseur ne doit pas ouvrir le profil de l'objet de prise en charge transmis dans l'appel. En outre, il ne doit pas inscrire un identificateur unique de fournisseur, enregistrer une ligne d'État ou renvoyer des données de connexion au spouleur MAPI.
    
5. Le fournisseur ne doit pas appeler **AddRef** pour l'objet de prise en charge, car il ne requiert pas de pointeur vers l'objet. 
    
Dans la mesure du possible, les fournisseurs doivent renvoyer les chaînes d'erreur et d'avertissement appropriées pour les appels **d'ouverture de session** , car cela facilite grandement la tâche des utilisateurs en déterminant la raison de l'échec de l'opération. Pour renvoyer ces chaînes, un fournisseur définit les membres dans la structure **MAPIERROR** . MAPI recherche, utilise et libère la structure **MAPIERROR** si elle est renvoyée par un fournisseur. 
  
La mémoire pour cette structure **MAPIERROR** doit être allouée à l'aide de la mémoire tampon passée dans _lpfAllocateBuffer_ sur l'appel **MSProviderInit** . Les chaînes d'erreur contenues dans la structure renvoyée doivent être au format Unicode si MAPI_UNICODE est défini dans le ulFlags **d'ouverture de session** _;_ sinon, elles doivent se trouver dans le jeu de caractères ANSI. 
  
Pour la plupart des valeurs d'erreur renvoyées à partir de l' **ouverture de session**, MAPI désactive les services de messagerie auxquels appartient le fournisseur. MAPI n'appelle aucun fournisseur appartenant à ces services pendant la durée de vie de la session MAPI. À l'inverse, lorsque l' **ouverture de session** renvoie la valeur d'erreur MAPI_E_FAILONEPROVIDER à partir de son ouverture de session, MAPI ne désactive pas le service de messagerie auquel le fournisseur appartient. L' **ouverture de session** doit renvoyer MAPI_E_FAILONEPROVIDER si elle rencontre une erreur qui ne garantit pas la désactivation du service entier pendant la durée de vie de la session. Par exemple, un fournisseur peut renvoyer cette erreur lorsqu'il n'autorise pas l'affichage d'une interface utilisateur et qu'un mot de passe requis n'est pas disponible. 
  
Si un fournisseur renvoie MAPI_E_UNCONFIGURED à partir de son ouverture de session, MAPI appelle la fonction d'entrée de service de message du fournisseur, puis tente à nouveau d'ouvrir une session. MAPI transmet MSG_SERVICE_CONFIGURE comme contexte pour permettre au service de se configurer lui-même. Si le client a choisi d'autoriser une interface utilisateur sur l'ouverture de session, le service peut présenter sa feuille de propriétés de configuration pour permettre à l'utilisateur d'entrer des informations de configuration.
  
## <a name="see-also"></a>Voir aussi



[IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md)
  
[IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md)
  
[IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)
  
[IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIERROR](mapierror.md)
  
[MSProviderInit](msproviderinit.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)

