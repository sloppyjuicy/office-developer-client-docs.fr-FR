---
title: IMSProviderLogon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMSProvider.Logon
api_type:
- COM
ms.assetid: 890d9cbe-3570-4cf0-aeae-667c0e5ba181
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 99022d5914881ff6ce2893c8f1d624d8c70efbec
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462812"
---
# <a name="imsproviderlogon"></a>IMSProvider::Logon

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Connecte MAPI à une instance d’un fournisseur de magasins de messages.
  
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
  
> [in] Pointeur vers l’objet de support MAPI actuel pour la magasin de messages.
    
 _ulUIParam_
  
> [in] Poignée vers la fenêtre parente de toutes les boîtes de dialogue ou fenêtres affichées par cette méthode. 
    
 _lpszProfileName_
  
> [in] Pointeur vers une chaîne qui contient le nom du profil utilisé pour l’ouverture de page du fournisseur de magasins. Cette chaîne peut être affichée dans des boîtes de dialogue, écrite dans un fichier journal ou simplement ignorée. Elle doit être au format Unicode si l’MAPI_UNICODE est définie dans _le paramètre ulFlags_ . 
    
 _cbEntryID_
  
> [in] Taille, en octets, de l’identificateur d’entrée pointé par  _le paramètre lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Pointeur vers l’identificateur d’entrée de la boutique de messages. La transmission **de la valeur null** dans  _lpEntryID_ indique qu’une magasin de messages n’a pas encore été sélectionnée et que les boîtes de dialogue qui permettent à l’utilisateur de sélectionner une magasin de messages peuvent être présentées. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle l’utilisation de l’logo. Les indicateurs suivants peuvent être définies :
    
MAPI_DEFERRED_ERRORS 
  
> L’appel est autorisé à réussir même si l’objet sous-jacent n’est pas disponible pour l’implémentation de l’appelant. Si l’objet n’est pas disponible, un appel ultérieur à l’objet peut occasioner une erreur.
    
MAPI_UNICODE 
  
> Les chaînes transmises sont au format Unicode. Si MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.
    
MDB_NO_DIALOG 
  
> Empêche l’affichage des boîtes de dialogue d’affichage. Si cet indicateur est définie, la valeur d’MAPI_E_LOGON_FAILED’erreur est renvoyée si l’échec de la logon. Si cet indicateur n’est pas définie, le fournisseur de la boutique de messages peut inviter l’utilisateur à corriger un nom ou un mot de passe, à insérer un disque ou à effectuer d’autres actions nécessaires pour établir une connexion à la boutique.
    
MDB_NO_MAIL 
  
> La magasin de messages ne doit pas être utilisée pour l’envoi ou la réception de messages. L’indicateur indique à MAPI de ne pas informer lepooler MAPI que cette magasin de messages est en cours d’ouverture. Si cet indicateur est définie et que la magasin de messages est étroitement associée à un fournisseur de transport, le fournisseur n’a pas besoin d’appeler la méthode [IMAPISupport::SpoolerNotify](imapisupport-spoolernotify.md) . 
    
MDB_TEMPORARY 
  
> Logs on the store so that information can be retrieved programmatically from the profile section, without use of dialog boxes. Cet indicateur indique à MAPI que la boutique ne doit pas être ajoutée à la table de la boutique de messages et que la boutique ne peut pas être rendue permanente. Si cet indicateur est définie, les fournisseurs de magasins de messages n’ont pas besoin d’appeler la méthode [IMAPISupport::ModifyProfile](imapisupport-modifyprofile.md) . 
    
MDB_WRITE 
  
> Demande une autorisation de lecture/écriture.
    
 _lpInterface_
  
> [in] Pointeur vers l’identificateur d’interface (IID) de connexion à la boutique de messages. La **transmission de la valeur null** indique que l’interface MAPI pour la magasin de messages ( [IMsgStore](imsgstoreimapiprop.md)) est renvoyée. Le  _paramètre lpInterface_ peut également être définie sur un identificateur pour une interface appropriée pour la magasin de messages (par exemple, IID_IUnknown ou IID_IMAPIProp). 
    
 _lpcbSpoolSecurity_
  
> [out] Pointeur vers la variable dans laquelle le fournisseur de magasins renvoie la taille, en octets, des données de validation dans le paramètre _lppbSpoolSecurity_ . 
    
 _lppbSpoolSecurity_
  
> [out] Pointeur vers le pointeur vers les données de validation renvoyées. Ces données de validation sont fournies afin que la méthode [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) puisse connecter lepooler MAPI au même magasin que le fournisseur de la boutique de messages. 
    
 _lppMAPIError_
  
> [out] Pointeur vers un pointeur vers la structure [MAPIERROR](mapierror.md) renvoyée, le caser, qui contient des informations de version, de composant et de contexte pour une erreur. Le  _paramètre lppMAPIError_ peut être définie sur **null** s’il n’existe aucune structure **MAPIERROR** à renvoyer. 
    
 _lppMSLogon_
  
> [out] Pointeur vers le pointeur vers l’objet d’ouverture de session de la boutique de messages pour que MAPI se connecte.
    
 _lppMDB_
  
> [out] Pointeur vers le pointeur vers l’objet de magasin de messages pour lepooler MAPI et les applications clientes à connecter.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_E_FAILONEPROVIDER 
  
> Ce fournisseur ne peut pas se connecter, mais cette erreur ne doit pas désactiver le service. 
    
MAPI_E_LOGON_FAILED 
  
> Une session d’ouverture de session n’a pas pu être établie.
    
MAPI_E_UNCONFIGURED 
  
> Le profil ne contient pas suffisamment d’informations pour que la logon soit terminée. Lorsque cette valeur est renvoyée, MAPI appelle la fonction de point d’entrée de service de message du fournisseur de messages.
    
MAPI_E_USER_CANCEL 
  
> L’utilisateur a annulé l’opération, généralement en cliquant sur le **bouton Annuler dans** une boîte de dialogue. 
    
MAPI_E_UNKNOWN_CPID 
  
> Le serveur n’est pas configuré pour prendre en charge la page de code du client.
    
MAPI_E_UNKNOWN_LCID 
  
> Le serveur n’est pas configuré pour prendre en charge les informations de paramètres régionaux du client.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais des informations d’erreur sont disponibles pour le fournisseur de la boutique de messages. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED’avertissement** . Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md). Pour obtenir les informations d’erreur du fournisseur, appelez la méthode [IMAPISession::GetLastError](imapisession-getlasterror.md) . 
    
## <a name="remarks"></a>Remarques

MAPI appelle la **méthode IMSProvider::Logon** pour faire la majorité du traitement nécessaire pour obtenir l’accès à une magasin de messages. Les fournisseurs de banque de messages valident les informations d’identification de l’utilisateur nécessaires pour accéder à une banque particulière et retournent un objet de banque de messages dans le paramètre _lppMDB_ à qui lepooler MAPI et les applications clientes peuvent se connecter. 
  
Outre l’objet de magasin de messages renvoyé pour l’utilisation du client et dupooler MAPI, le fournisseur renvoie également un objet d’ouverture de la boutique de messages que MAPI utilisera pour contrôler la boutique ouverte. L’objet d’ouverture de la boutique de messages et l’objet de la boutique de messages doivent être étroitement liés à l’intérieur du fournisseur de la boutique de messages afin que chacun puisse affecter l’autre. L’utilisation de l’objet store et de l’objet d’ouverture de connecté doit être identique ; il doit y avoir une correspondance un-à-un entre l’objet d’ouverture de ligne et l’objet store afin que les objets agissent comme s’il s’agit d’un objet qui expose deux interfaces. Les deux objets doivent également être créés ensemble et libérés ensemble. 
  
L’objet de prise en charge MAPI, créé par MAPI et transmis au fournisseur dans le paramètre _lpMAPISup_ , fournit l’accès aux fonctions dans MAPI dont le fournisseur a besoin. Il s’agit notamment de fonctions qui enregistrent et récupèrent des informations de profil, des carnets d’adresses d’accès, etc. Le  _pointeur lpMAPISup_ peut être différent pour chaque magasin ouvert. Lors du traitement des appels pour une magasin de messages après l’ouverture de contrat, le fournisseur de la boutique doit utiliser la variable  _lpMAPISup_ spécifique à cette boutique. Pour tout  appel d’ouverture de conférence qui ouvre une magasin de messages et parvient à créer un objet d’ouverture de conférence de la boutique de messages, le fournisseur doit enregistrer un pointeur vers l’objet de support MAPI dans l’objet d’ouverture de conférence de la boutique et doit appeler la méthode [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) pour ajouter une référence à l’objet de support. 
  
Le  _paramètre ulUIParam_ doit être utilisé si le fournisseur présente des boîtes de dialogue pendant **l’appel d’accès** . Toutefois, les boîtes de dialogue ne doivent pas être présentées si  _ulFlags_ contient l’MDB_NO_DIALOG’indicateur. Si une interface utilisateur doit être appelée mais  _que ulFlags_ ne l’autorise pas, ou si, pour une autre raison, une interface utilisateur ne peut pas être affichée, le fournisseur doit renvoyer MAPI_E_LOGON_FAILED. Si **l’utilisateur** affiche une boîte de dialogue et que l’utilisateur l’annule, généralement en cliquant sur le bouton Annuler  de la boîte de dialogue, le fournisseur doit MAPI_E_USER_CANCEL. 
  
Le  _paramètre lpEntryID_ peut être **null** ou pointer vers un identificateur d’entrée de magasin non veloppé précédemment créé par cette magasin de messages. Si  _lpEntryID_ pointe vers un identificateur d’entrée non veloppé, cet identificateur d’entrée peut être issu de l’un des différents endroits : 
  
- Il peut s’agit d’un identificateur d’entrée que le fournisseur de **magasin a** précédemment enveloppé et écrit dans la section de profil sous la PR_ENTRYID ([PidTagEntryId](pidtagentryid-canonical-property.md)).
    
- Il peut s’agit d’un identificateur d’entrée que le fournisseur a précédemment enveloppé et renvoyé à un client appelant en tant que **propriété PR_STORE_ENTRYID** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)). 
    
- Il peut s’agit d’un identificateur d’entrée que le fournisseur a précédemment enveloppé et renvoyé à un client appelant en tant que propriété PR_ENTRYID d’un objet de la boutique de messages. 
    
Dans tous ces cas, il est possible que l’identificateur d’entrée a été créé sur un autre ordinateur que celui actuellement utilisé.
  
Lorsque  _lpEntryID_ n’est pas **null**, il doit contenir toutes les informations nécessaires pour identifier et localiser la magasin de messages. Ces informations peuvent inclure des noms de volume réseau, des numéros de téléphone, des noms de comptes d’utilisateurs, etc. Si la connexion au magasin ne peut pas être réalisée à l’aide des données de l’identificateur d’entrée, le fournisseur de magasin doit afficher une boîte de dialogue qui permet à l’utilisateur de sélectionner le magasin à ouvrir. Une boîte de dialogue peut être requise, par exemple, si un serveur a été renommé, si un nom de compte a changé ou si des parties du réseau ne sont pas disponibles.
  
Lorsque  _lpEntryID_ est **null**, la magasin de messages à utiliser n’a pas encore été sélectionnée. Le fournisseur peut toujours accéder à un magasin sans afficher de boîte de dialogue s’il prend en charge d’autres méthodes pour spécifier le magasin. Par exemple, le fournisseur peut vérifier son fichier d’initialisation ou rechercher des propriétés supplémentaires qui ont été placées dans sa section de profil ou dans la section de profil de son service de messagerie lors de la configuration.
  
Si un fournisseur trouve que toutes les informations requises ne se trouvent pas dans le profil, il doit renvoyer MAPI_E_UNCONFIGURED. MAPI appelle ensuite la fonction de point d’entrée du service de messagerie du fournisseur pour permettre à l’utilisateur de sélectionner une banque, voire d’en créer une, et d’entrer un nom de compte et un mot de passe, si nécessaire. MAPI crée automatiquement une section de profil pour une nouvelle boutique . Cette nouvelle section de profil peut être temporaire ou permanente, selon la façon dont elle a été ajoutée. Si le fournisseur de magasin appelle la méthode **IMAPISupport::ModifyProfile** , la nouvelle section de profil devient permanente et le magasin est ajouté à la liste des magasins de messages renvoyé par la méthode [IMAPISession::GetMsgStoresTable](imapisession-getmsgstorestable.md) . 
  
Le  _paramètre lpInterface_ spécifie l’IID de l’interface requise pour l’objet store nouvellement ouvert. La **transmission de la valeur null**  _dans lpInterface_ spécifie que l’interface de magasin de messages MAPI, **IMsgStore**, est requise. La transmission de l’objet de IID_IMsgStore, spécifie également que **IMsgStore** est requis. Si IID_IUnknown est transmis dans  _lpInterface_, le fournisseur doit ouvrir le magasin à l’aide de l’interface dérivée [d’IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx) qui convient le mieux au fournisseur (là encore, il s’agit généralement **d’IMsgStore**). Lorsque IID_IUnknown est passé, l’implémentation d’appel utilise la méthode [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) pour sélectionner une interface après la réussite de l’opération d’ouverture de la boutique. 
  
L’appel **IMSProvider::Logon** doit renvoyer suffisamment d’informations, telles qu’un chemin d’accès au magasin et des informations d’identification pour accéder au magasin, pour permettre aupooler MAPI de se connecter à la même boutique que le fournisseur de magasins sans présenter de boîte de dialogue. Les  _paramètres lpcbSpoolSecurity_ et  _lppbSpoolSecurity_ sont utilisés pour renvoyer ces informations. Le fournisseur alloue la mémoire pour ces données en passant un pointeur vers une mémoire tampon dans le paramètre _lpfAllocateBuffer_ de la fonction [MSProviderInit](msproviderinit.md) ; le fournisseur place la taille de cette mémoire tampon dans _lpcbSpoolSecurity_. 
  
MAPI libère cette mémoire tampon, le cas échéant. Si l’ouverture de page du spouleur MAPI dans le magasin peut être accomplie à partir des informations de la section profil uniquement, le fournisseur peut renvoyer null dans  _lppbSpoolSecurity_ et 0 pour la taille des informations dans  _lpcbSpoolSecurity_. L’ouverture de logo dupooler MAPI se produit dans le cadre d’un processus différent de celui de l’ouverture de la boutique . Étant donné que la mémoire tampon qui contient les informations transmises est copiée entre les processus, il se peut qu’elle ne se trouve pas en mémoire au même emplacement pour le processus dupooler MAPI que pour le processus du fournisseur de magasins. Par conséquent, un fournisseur ne doit pas placer d’adresses dans cette mémoire tampon. Pour plus d’informations sur l’logo dupooler MAPI, voir la méthode [IMSProvider::SpoolerLogon](imsprovider-spoolerlogon.md) . 
  
La plupart des fournisseurs de magasins utilisent la méthode [IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) de l’objet de support transmis dans le paramètre _lpMAPISup_ pour enregistrer et récupérer les informations d’identification et les options de l’utilisateur. **OpenProfileSection** permet à un fournisseur de magasin d’enregistrer des informations arbitraires supplémentaires dans une section de profil et de les associer à une ressource particulière. Par exemple, un fournisseur de banque d’informations peut enregistrer le nom du compte d’utilisateur et le mot de passe associés à une ressource, ainsi que les chemins d’accès ou autres informations nécessaires pour accéder à cette ressource. 
  
Les propriétés dont les identificateurs de propriétés 0x6600 via 0x67FF sont des propriétés sécurisées disponibles pour le fournisseur pour son propre usage afin de stocker des données privées dans des sections de profil. Pour plus d’informations sur les utilisations des propriétés dans les objets de section de profil, voir la méthode [IProfSect : IMAPIProp](iprofsectimapiprop.md) . 
  
Outre les données privées dans les propriétés avec des identificateurs 0x6600 via 0x67FF, le fournisseur de banque doit fournir des informations pour la propriété **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) dans sa section de profil. Il doit placer dans **PR_DISPLAY_NAME** le nom complet du fournisseur lui-même , une chaîne d’identification (par exemple, « Microsoft Personal Information Store ») qui s’affiche pour les utilisateurs afin qu’ils peuvent distinguer ce magasin de messages des autres personnes à qui ils ont peut-être accès. **PR_DISPLAY_NAME** contient généralement un nom de serveur, un nom de compte d’utilisateur ou un chemin d’accès. 
  
Certaines propriétés de section de profil sont visibles dans la table de la boutique de messages . d’autres sont visibles pendant l’installation, l’installation et la configuration du sous-système MAPI. Le fournisseur fournit généralement des informations pour ces propriétés visibles à la fois pour une nouvelle section de profil, qui n’inclut pas encore les informations d’identification enregistrées ou les informations privées, et lorsqu’il trouve que les informations de propriété ont changé. Pour plus d’informations sur les sections de profil, voir [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md).
  
Après avoir correctement journalé un utilisateur et avant de revenir à MAPI, le fournisseur de magasins doit créer le tableau des propriétés de la ligne d’état de la ressource et appeler la méthode [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) . 
  
 **Les appels d’ouverture** de session qui ouvrent des magasins de messages déjà ouverts pour la session MAPI en cours ignorent une grande partie du traitement décrit précédemment. Ces appels ne créent pas de lignes d’état, ne retournent pas d’objets d’ouverture de conférence de la boutique de messages, appellent **AddRef** pour l’objet de support MAPI ou ne retournent pas de données pour l’ouverture de conférence dupooler MAPI. Ces appels ne retournent pas S_OK et retournent un objet de magasin de messages avec l’interface demandée. 
  
Pour détecter ces appels, le fournisseur doit conserver une liste dans l’objet fournisseur de la boutique de messages des magasins déjà ouverts pour cet objet fournisseur. Lors du traitement **d’un appel d’ouverture** de session, le fournisseur doit analyser cette liste de magasins ouverts et déterminer si la boutique à ouvrir est déjà ouverte. Si c’est le cas, les informations d’identification de l’utilisateur n’ont pas besoin d’être cochées et l’affichage d’une boîte de dialogue doit être évité, si possible. Si des boîtes de dialogue doivent être affichées, le fournisseur doit vérifier les informations renvoyées pour voir si un magasin a été ouvert une deuxième fois. En outre, le fournisseur doit vérifier les ouvertures en double à l’aide de  _lpEntryID_ au début du traitement des appels **d’ouverture** de conférence. 
  
Le traitement standard d’un appel **d’ouverture** de conférence qui accède à une boutique ouverte est le suivant : 
  
1. Le fournisseur de magasin appelle **AddRef** pour l’objet store existant si la nouvelle interface demandée est identique à l’interface du magasin existant. Sinon, il appelle **QueryInterface** pour obtenir la nouvelle interface. Si le magasin ne prend pas en charge la nouvelle interface, le fournisseur doit renvoyer la valeur d’erreur MAPI_E_INTERFACE_NOT_SUPPORTED. 
    
2. Le fournisseur renvoie un pointeur vers l’interface requise de l’objet store existant dans  _lppMDB_.
    
3. Le fournisseur renvoie **la valeur null** dans  _lppMSLogon_.
    
4. Le fournisseur ne doit pas ouvrir le profil de l’objet de support transmis dans l’appel. En outre, il ne doit pas inscrire un identificateur unique de fournisseur, inscrire une ligne d’état ou renvoyer des données d’accès aupooler MAPI.
    
5. Le fournisseur ne doit pas **appeler AddRef** pour l’objet de support, car il ne nécessite pas de pointeur vers l’objet. 
    
Dans la mesure du possible, les fournisseurs doivent renvoyer les chaînes d’erreur et d’avertissement appropriées pour les appels d’accès, car cela permet aux utilisateurs de déterminer pourquoi quelque chose n’a pas fonctionné. Pour renvoyer ces chaînes, un fournisseur définit les membres dans la structure **MAPIERROR** . MAPI recherche, utilise et libère la structure **MAPIERROR** si elle est renvoyée par un fournisseur. 
  
La mémoire de cette structure **MAPIERROR** doit être allouée à l’aide de la mémoire tampon transmise dans  _lpfAllocateBuffer_ lors de l’appel **MSProviderInit** . Toutes les chaînes d’erreur contenues dans la structure renvoyée doivent être au format Unicode si MAPI_UNICODE est définie dans les _ulFlags_ **logon** ; sinon, elles doivent être dans le jeu de caractères ANSI. 
  
Pour la plupart des valeurs d’erreur renvoyées par **la propriété Logon**, MAPI désactive les services de messagerie auquel appartient le fournisseur défaillant. MAPI n’appellera aucun fournisseur qui appartient à ces services pendant toute la durée de la session MAPI. En revanche, lorsque **Logon** renvoie la valeur d’erreur MAPI_E_FAILONEPROVIDER à partir de sa logon, MAPI ne désactive pas le service de messagerie auquel le fournisseur appartient. **L’ouverture** de session doit MAPI_E_FAILONEPROVIDER si elle rencontre une erreur qui ne justifie pas la désactivation de l’intégralité du service pendant toute la durée de la session. Par exemple, un fournisseur peut renvoyer cette erreur lorsqu’il n’autorise pas l’affichage d’une interface utilisateur et qu’un mot de passe requis n’est pas disponible. 
  
Si un fournisseur renvoie MAPI_E_UNCONFIGURED à partir de sa logon, MAPI appelle la fonction d’entrée de service de messagerie du fournisseur, puis réessaye d’y revenir. MAPI passe MSG_SERVICE_CONFIGURE comme contexte pour donner au service la possibilité de se configurer lui-même. Si le client a choisi d’autoriser une interface utilisateur sur la logon, le service peut présenter sa feuille de propriétés de configuration afin que l’utilisateur puisse entrer des informations de configuration.
  
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

