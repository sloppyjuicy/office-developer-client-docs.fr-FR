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
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9c7f62c69c7a06f7ca0e4bfddcf789cddc536ea6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386564"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Journaux MAPI sur une instance d’un fournisseur de magasin de message.
  
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
  
> [in] Un pointeur vers l’interface MAPI en cours prend en charge l’objet de la banque de messages.
    
 _ulUIParam_
  
> [in] Un handle vers la fenêtre parent des boîtes de dialogue ni windows cette méthode affiche. 
    
 _lpszProfileName_
  
> [in] Pointeur vers une chaîne qui contient le nom du profil utilisé pour la connexion au fournisseur du magasin. Cette chaîne peut être affichée dans les boîtes de dialogue, écrite dans un fichier journal ou ignorée. Si l’indicateur MAPI_UNICODE est défini dans le paramètre _ulFlags_ , elle doit être au format Unicode. 
    
 _cbEntryID_
  
> [in] La taille, en octets, de l’identificateur d’entrée indiqué par le paramètre _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de la banque de messages. En passant **null** _lpEntryID_ indique qu’une banque de messages n’a pas encore été sélectionnée et que les boîtes de dialogue permettant à l’utilisateur de sélectionner une banque de messages peuvent être présentées. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle la façon dont les paramètres de connexion est effectuée. Les indicateurs suivants peuvent être définis :
    
MAPI_DEFERRED_ERRORS 
  
> L’appel est autorisé à fonctionne même si l’objet sous-jacent n’est pas disponible pour l’implémentation d’appel. Si l’objet n’est pas disponible, un appel à l’objet suivant peut déclencher une erreur.
    
MAPI_UNICODE 
  
> Les chaînes passée sont au format Unicode. Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
MDB_NO_DIALOG 
  
> Empêche l’affichage des boîtes de dialogue d’ouverture de session. Si cet indicateur est défini, la valeur d’erreur MAPI_E_LOGON_FAILED est renvoyée si l’ouverture de session échoue. Si cet indicateur n’est pas défini, le fournisseur de banque de message peut inviter l’utilisateur à corriger un nom ou le mot de passe, à insérer un disque ou à effectuer d’autres actions sont nécessaires pour établir une connexion à la base.
    
MDB_NO_MAIL 
  
> La banque de messages ne doit pas être utilisée pour envoyer ou recevoir de courrier. L’indicateur signale MAPI ne pas pour notifier le spouleur MAPI que cette banque de messages est en cours d’ouverture. Si cet indicateur est défini et que la banque de messages est fortement couplée à un fournisseur de transport, le fournisseur n’a pas besoin d’appeler la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . 
    
MDB_TEMPORARY 
  
> Journaux sur le magasin afin que les informations peuvent être récupérées par programme dans la section profil, sans utilisent de boîtes de dialogue. Cet indicateur ordonne à MAPI que le magasin ne doit ne pas être ajouté à la table et que le magasin ne peut être permanent. Si cet indicateur est défini, les fournisseurs de magasins de message est inutile d’appeler la méthode [IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md) . 
    
MDB_WRITE 
  
> Demandes d’autorisation de lecture/écriture.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) pour la banque de messages pour vous connecter à. Le passage de **null** indique l’interface MAPI pour la banque de messages ( [IMsgStore](imsgstoreimapiprop.md)) est renvoyée. Le paramètre _lpInterface_ peut également être défini à un identificateur pour une interface appropriée pour la banque de messages (par exemple, IID_IUnknown ou IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [out] Pointeur vers la variable dans laquelle le fournisseur de banque renvoie la taille, en octets, des données de validation dans le paramètre _lppbSpoolSecurity_ . 
    
 _lppbSpoolSecurity_
  
> [out] Pointeur vers le pointeur vers les données retournées validation. Ces données de validation sont fournies afin que la méthode [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) peut se connecter le spouleur MAPI sur le même magasin en tant que le fournisseur de banque de messages. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la [MAPIERROR](mapierror.md) structure retournée, le cas échéant, qui contient des informations de version, composant et le contexte d’une erreur. Le paramètre _lppMAPIError_ peut avoir pour **valeur null** s’il n’existe aucune structure **MAPIERROR** à renvoyer. 
    
 _lppMSLogon_
  
> [out] Un pointeur vers le pointeur vers le message stocker l’objet d’ouverture de session MAPI pour vous connecter à.
    
 _lppMDB_
  
> [out] Un pointeur vers le pointeur vers le message stocker d’objet pour les applications clientes pour vous connecter à spouleur MAPI.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
RÉFÉRENCE À MAPI_E_FAILONEPROVIDER 
  
> Ce fournisseur ne peut pas se connecter, mais cette erreur ne doit pas désactiver le service. 
    
MAPI_E_LOGON_FAILED 
  
> Une ouverture de session n’a pas pu être établie.
    
MAPI_E_UNCONFIGURED 
  
> Le profil ne contient pas de suffisamment d’informations pour l’ouverture de session Terminer. Lorsque cette valeur est renvoyée, MAPI appelle la fonction de point d’entrée du message-service du fournisseur de banque de messages.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération de généralement en cliquant sur le bouton **Annuler** dans une boîte de dialogue. 
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n’est pas configuré pour prendre en charge de la page de codes du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais le fournisseur de banque de messages a des informations d’erreur disponibles. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme étant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de Macros pour gérer les erreurs](using-macros-for-error-handling.md). Pour obtenir les informations d’erreur à partir du fournisseur, appelez la méthode [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Remarques

MAPI appelle la méthode **IMSProvider::Logon** pour l’essentiel du traitement nécessaire pour obtenir l’accès à une banque de messages. Fournisseurs de banque de messages valider les informations d’identification nécessaires pour accéder à un magasin particulier et renvoyer un objet de banque de messages dans le paramètre _lppMDB_ que les applications de client et spouleur MAPI peuvent ouvrir une session sur utilisateur. 
  
En plus de l’objet de banque de message renvoyé pour le client et l’utilisation de spouleur MAPI, le fournisseur renvoie également un objet de d’ouverture de session du magasin de message MAPI à utiliser dans le contrôle de la banque ouverte. L’objet d’ouverture de session du magasin de message et l’objet de banque de messages doivent être étroitement liés à l’intérieur du fournisseur de banque de message afin que chacun peut avoir une incidence sur l’autre. L’utilisation de l’objet de magasin et l’objet d’ouverture de session doit être identique ; une correspondance entre l’objet d’ouverture de session et l’objet de magasin doit être tels que les objets se comportent comme s’ils étaient un seul objet qui expose les deux interfaces. Les deux objets doivent également être créés ensemble et libérés ensemble. 
  
L’objet de prise en charge MAPI, créé par MAPI et transmis au fournisseur dans le paramètre _lpMAPISup_ , permet d’accéder aux fonctions MAPI qui requiert le fournisseur. Cela inclut les fonctions qu’enregistrent et récupérer des informations de profil, accéder aux carnets d’adresses et ainsi de suite. Le pointeur _lpMAPISup_ peut être différent pour chaque magasin est ouvert. Pendant le traitement des appels pour une banque de messages après l’ouverture de session, le fournisseur de magasin doit utiliser la variable _lpMAPISup_ qui est spécifique à cette banque. Pour chaque appel **d’ouverture de session** qui ouvre une banque de messages et réussit lors de la création d’un objet d’ouverture de session du magasin de message, le fournisseur doit enregistrer un pointeur vers l’objet de prise en charge MAPI dans l’objet d’ouverture de session du magasin et devez appeler la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour ajouter une référence l’objet de prise en charge. 
  
Le paramètre _ulUIParam_ doit être utilisé si le fournisseur présente des boîtes de dialogue lors de l’appel **d’ouverture de session** . Toutefois, les boîtes de dialogue ne doivent pas être présentés si _ulFlags_ contient l’indicateur MDB_NO_DIALOG. Si une interface utilisateur doit être appelée mais _ulFlags_ ne l’autorise pas, ou si une interface utilisateur ne peut pas être affichée pour une raison quelconque, le fournisseur doit renvoyer MAPI_E_LOGON_FAILED. Si **l’ouverture de session** affiche une boîte de dialogue et l’utilisateur annule l’ouverture de session, généralement en cliquant sur le bouton **Annuler** de la boîte de dialogue, le fournisseur doit retourner MAPI_E_USER_CANCEL. 
  
Le paramètre _lpEntryID_ peut être **null** ou pointez sur un magasin non identificateur d’entrée qui stockent ce message créé précédemment. Si _lpEntryID_ pointe vers un identificateur d’entrée non, cet identificateur d’entrée peut provenir de plusieurs emplacements : 
  
- Il peut être un identificateur d’entrée que le fournisseur de banque précédemment encapsulé et écrit à la section profil comme une propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Il peut être un identificateur d’entrée qui le fournisseur précédemment encapsulé et retournées à un client appelant comme une propriété **PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Il peut être un identificateur d’entrée qui le fournisseur précédemment encapsulé et retournées à un client appelant que la propriété **PR_ENTRYID** d’un objet de banque de messages. 
    
Dans chacun de ces cas, il est possible que l’identificateur d’entrée a été créé sur un autre ordinateur que celui en cours d’utilisation.
  
Lorsque _lpEntryID_ n’est pas **null**, il doit contenir toutes les informations nécessaires pour identifier et localiser la banque de messages. Ces informations peuvent inclure des noms de volume réseau, numéros de téléphone, noms de compte d’utilisateur et ainsi de suite. Si la connexion à la base ne peut pas être effectuée en utilisant les données dans l’identificateur d’entrée, le fournisseur de banque doit afficher une boîte de dialogue qui permet à l’utilisateur de sélectionner le magasin à ouvrir. Une boîte de dialogue peut être requise, par exemple, si un serveur a été renommé, un nom de compte a été modifiée ou certaines parties du réseau ne sont pas disponibles.
  
Lorsque _lpEntryID_ a la **valeur null**, à utiliser la banque de messages n’a pas encore été sélectionnée. Le fournisseur peut toujours accéder à un magasin sans afficher une boîte de dialogue si elle prend en charge d’autres méthodes pour spécifier le magasin. Par exemple, le fournisseur peut vérifier son fichier d’initialisation, ou il peut rechercher des propriétés supplémentaires qui ont été placées dans la section profil de son ou son message du service à la configuration.
  
Si un fournisseur qui recherche toutes les informations requises ne sont pas dans le profil, elle doit retourner MAPI_E_UNCONFIGURED. MAPI appelle ensuite la fonction de point d’entrée du fournisseur message service pour permettre à l’utilisateur pour sélectionner un magasin, ou en créer une, et pour entrer un nom de compte et le mot de passe, comme nécessaire. MAPI crée automatiquement une nouvelle section de profil pour un nouveau magasin ; Cette nouvelle section de profil peut être temporaire ou permanent, selon la façon dont il a été ajouté. Si le fournisseur de banque appelle la méthode **IMAPISupport::ModifyProfile** , la nouvelle section profil devient permanente et la banque est ajoutée à la liste des magasins de message renvoyé par la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Le paramètre _lpInterface_ Spécifie l’IID de l’interface requise pour l’objet magasin récemment ouverte. Le passage de **null** dans _lpInterface_ Spécifie que l’interface de banque de message MAPI, **IMsgStore**, est requis. En passant l’objet de banque de messages, IID_IMsgStore, indique également que **IMsgStore** est requis. Si IID_IUnknown est passé dans _lpInterface_, le fournisseur doit ouvrir le magasin à l’aide de n’importe quel interface dérivée de [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) est recommandé pour le fournisseur (là encore, il s’agit généralement **IMsgStore**). Lorsque IID_IUnknown est passé, l’implémentation appelante utilise la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) pour sélectionner une interface une fois l’opération d’ouverture magasin réussit. 
  
L’appel **IMSProvider::Logon** doit renvoyer suffisamment d’informations, telles que le magasin et les informations d’identification pour l’accès au magasin, pour autoriser le spouleur MAPI ouvrir une session sur le même magasin que le fournisseur de banque sans présenter une boîte de dialogue chemin d’accès. Les paramètres _lpcbSpoolSecurity_ et _lppbSpoolSecurity_ permettent de renvoyer ces informations. Le fournisseur alloue de la mémoire pour ces données en passant un pointeur vers un tampon dans [MSProviderInit](msproviderinit.md) _lpfAllocateBuffer_ paramètre de la fonction ; le fournisseur place la taille de ce tampon dans _lpcbSpoolSecurity_. 
  
MAPI libère ce tampon, le cas échéant. Si l’ouverture de session du spouleur MAPI dans le magasin peut être réalisé à partir des informations dans la section profil uniquement, le fournisseur peut retourner null dans _lppbSpoolSecurity_ et 0 pour la taille de l’information dans _lpcbSpoolSecurity_. L’ouverture de session MAPI spouleur se produit dans le cadre d’un processus différent de l’ouverture de session du magasin ; parce que la mémoire tampon qui contient les informations passées obtient copié entre les processus, il peut être pas en mémoire au même emplacement pour le processus de spouleur MAPI que pour le processus de fournisseur de banque. Par conséquent, un fournisseur ne doit pas mettre les adresses dans cet mémoire tampon. Pour plus d’informations sur l’ouverture de session MAPI spouleur, voir la méthode [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) . 
  
La plupart des fournisseurs de magasins d’utilisent la méthode [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) de l’objet de prise en charge passé dans le paramètre _lpMAPISup_ pour l’enregistrement et la récupération des options et des informations d’identification de l’utilisateur. **OpenProfileSection** permet à un fournisseur de magasin enregistrer des informations supplémentaires arbitraires dans une section de profil et l’associer à une ressource particulière. Par exemple, un fournisseur de magasins permettre enregistrer le nom de compte d’utilisateur et le mot de passe associé à une ressource et des chemins d’accès ou autres informations nécessaires pour accéder à cette ressource. 
  
Propriétés avec des identificateurs de propriété 0x6600 via 0x67FF sont sécurisées propriétés disponibles pour le fournisseur pour son propre permet de stocker des données privées dans les sections de profil. Pour plus d’informations sur l’utilisation des propriétés dans les objets section profil, voir la [IProfSect : IMAPIProp](iprofsectimapiprop.md) méthode. 
  
Outre les données privées dans les propriétés avec des identificateurs 0x6600 via 0x67FF, le fournisseur de banque doit fournir les informations de la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans la section profil. Il doit placer dans **PR_DISPLAY_NAME** le nom complet du fournisseur lui-même, une chaîne d’identification (par exemple, « Microsoft Personal Information Store ») qui est affichée pour les utilisateurs afin qu’ils peuvent faire la distinction cette banque de messages à partir d’autres personnes auxquelles ils peuvent avoir accéder À. **PR_DISPLAY_NAME** contient généralement un nom de serveur, le nom du compte utilisateur ou le chemin. 
  
Certaines propriétés de la section profil sont visibles dans le tableau de banque de messages ; d’autres personnes sont visibles pendant le programme d’installation, l’installation et configuration du sous-système MAPI. En règle générale, le fournisseur fournit des informations pour ces propriétés visibles à la fois pour une nouvelle section de profil, qui n’inclut pas encore enregistrées les informations d’identification ou des informations privées et s’il détecte que des informations sur la propriété a été modifiée. Pour plus d’informations sur les sections de profil, voir [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Une fois connecté à un utilisateur et avant le retour à MAPI, le fournisseur de magasin doit créer le tableau de propriétés pour la ligne d’état de la ressource et appelez la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . 
  
 Appels **d’ouverture de session** qui ouvrent des banques de messages qui sont déjà ouvertes pour la session MAPI en cours passez une grande partie du traitement décrit précédemment. Ces appels ne pas créer l’état des lignes, renvoient des objets de message banque d’ouverture de session, d’appeler **AddRef** pour l’objet de prise en charge MAPI ou renvoyer des données à l’ouverture de session MAPI spouleur. Ces appels retournent S_OK et renvoyer un objet banque de message avec l’interface demandée. 
  
Pour détecter des appels, le fournisseur doit gérer une liste dans l’objet de fournisseur de magasin de message des magasins déjà ouvert pour cet objet fournisseur. Lors du traitement d’un appel **d’ouverture de session** , le fournisseur doit analyser cette liste des magasins open et déterminer si le magasin de s’y connecter est déjà ouvert. S’il s’agit, informations d’identification utilisateur n’avez pas besoin à contrôler l’affichage d’une boîte de dialogue doit être évitée, si possible. Si les boîtes de dialogue doivent être affichées, le fournisseur doit vérifier les informations renvoyées pour voir si une banque a été ouvert une deuxième fois. En outre, le fournisseur doit vérifier les ouvertures en double à l’aide de _lpEntryID_ au début de l’appel **d’ouverture de session** de traitement. 
  
Traitement d’un appel **d’ouverture de session** qui accède à un magasin open standard est la suivante : 
  
1. Le fournisseur de banque appelle **AddRef** pour l’objet store existant si la nouvelle interface demandée est identique à l’interface pour le magasin existant. Sinon, elle appelle **QueryInterface** pour obtenir la nouvelle interface. Si le magasin ne prend pas en charge la nouvelle interface, le fournisseur doit retourner la valeur d’erreur MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Le fournisseur retourne un pointeur vers l’interface de l’objet store existant dans _lppMDB_requis.
    
3. Le fournisseur retourne **null** dans _lppMSLogon_.
    
4. Le fournisseur ne doit pas ouvrir le profil de l’objet de prise en charge passé l’appel. En outre, il ne doit pas inscrire un identificateur unique du fournisseur, d’inscrire une ligne d’état ou renvoyer des données d’ouverture de session spouleur MAPI.
    
5. Le fournisseur ne doit pas appeler **AddRef** pour l’objet de prise en charge, car elle ne nécessite pas un pointeur vers l’objet. 
    
La mesure du possible, fournisseurs doivent renvoyer une erreur appropriée et avertissement chaînes pour les appels **d’ouverture de session** , car cela considérablement facilite les tâches des utilisateurs pour déterminer pourquoi quelque chose n’a pas fonctionné. Pour renvoyer ces chaînes, un fournisseur définit les membres de la structure **MAPIERROR** . MAPI recherche utilise et libère de la structure **MAPIERROR** si elle est retournée par un fournisseur. 
  
La mémoire pour cette structure **MAPIERROR** doit être allouée à l’aide de la mémoire tampon passé sur l’appel de **MSProviderInit** _lpfAllocateBuffer_ . Toute erreur chaînes contenues dans la structure retournée doivent être au format Unicode si MAPI_UNICODE est définie dans l' **ouverture de session** _ulFlags ;_ sinon, ils doivent être dans le caractère ANSI définis. 
  
Pour la plupart des valeurs d’erreur renvoyés à partir de **l’ouverture de session**MAPI désactive les services de messagerie à laquelle appartient le fournisseur défectueux. MAPI ne sera pas appeler tous les fournisseurs qui appartiennent à ces services pour la durée de vie de la session MAPI. En revanche, lors de **l’ouverture de session** renvoie la valeur d’erreur de référence à MAPI_E_FAILONEPROVIDER à partir de son ouverture de session, MAPI ne désactive pas le service de message à laquelle appartient le fournisseur. **Ouverture de session** doit renvoyer la référence à MAPI_E_FAILONEPROVIDER si elle rencontre une erreur qui ne garantit pas la désactivation de l’ensemble du service pour la durée de vie de la session. Par exemple, un fournisseur peut retourner cette erreur lorsqu’il n’autorise pas l’affichage d’une interface utilisateur et un mot de passe requis n’est pas disponible. 
  
Si un fournisseur renvoie MAPI_E_UNCONFIGURED à partir de son ouverture de session, MAPI sont alors appeler la fonction de l’entrée de service de message du fournisseur et recommencez l’ouverture de session. MAPI passe MSG_SERVICE_CONFIGURE comme le contexte pour le service de donner la possibilité de configurer lui-même. Si le client a choisi d’autoriser une interface utilisateur à l’ouverture de session, le service peut représenter sa feuille de propriétés de configuration afin que l’utilisateur peut entrer des informations de configuration.
  
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

