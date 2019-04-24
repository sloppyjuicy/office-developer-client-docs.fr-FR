---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 2c8244180a5cafedc887fa72f36f233fb5084f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316631"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Rend permanentes toutes les modifications qui ont été apportées à un objet depuis la dernière opération d'enregistrement. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> dans Masque de des indicateurs qui contrôle le déroulement de l'objet lors de l'appel à la méthode **IMAPIProp:: SaveChanges** . Les indicateurs suivants peuvent être définis: 
    
NON_EMS_XP_SAVE
  
> Indique que le message n'a pas été remis à partir d'un serveur Microsoft Exchange. Cet indicateur doit être utilisé en combinaison avec la méthode [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) et l'indicateur ITEMPROC_FORCE pour indiquer à un magasin PST que le message est éligible pour le traitement des règles avant que le magasin de fichiers de dossiers personnels (PST) ne le signale écoute du client que le message est arrivé. Ce traitement des règles s'applique uniquement aux nouveaux messages créés avec [IMAPIFolder: CreateMessage](imapifolder-createmessage.md) sur un serveur qui n'est pas un serveur Exchange, auquel cas le serveur Exchange aurait déjà traité les règles sur le message. 
    
FORCE_SAVE 
  
> Les modifications doivent être écrites dans l'objet, en substituant toutes les modifications antérieures apportées à l'objet et l'objet doit être fermé. L'autorisation de lecture/écriture doit être définie pour que l'opération réussisse. L'indicateur FORCE_SAVE est utilisé après qu'un appel précédent de **SaveChanges** a retourné MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> Les modifications doivent être validées et l'objet doit être maintenu ouvert en lecture. Aucune modification supplémentaire n'est effectuée. 
    
KEEP_OPEN_READWRITE 
  
> Les modifications doivent être validées et l'objet doit être maintenu ouvert pour les autorisations en lecture/écriture. Cet indicateur est généralement défini lors de la première ouverture de l'objet pour autorisation de lecture/écriture. Les modifications ultérieures apportées à l'objet sont autorisées. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet le renvoi réussi de **SaveChanges** , éventuellement avant la validation complète des modifications. 
    
SPAMFILTER_ONSAVE
  
> Active le filtrage du courrier indésirable sur un message en cours d'enregistrement. La prise en charge du filtrage du courrier indésirable n’est disponible que si le type d’adresse e-mail de l’expéditeur suit le protocole SMTP et que le message est enregistré dans une banque pour un fichier de dossiers personnels (PST).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L'engagement des modifications a réussi.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges** ne peut pas conserver l'objet ouvert pour une autorisation en lecture seule si KEEP_OPEN_READONLY est défini ou une autorisation en lecture/écriture si KEEP_OPEN_READWRITE est défini. Aucune modification n'est validée. 
    
MAPI_E_OBJECT_CHANGED 
  
> L'objet a été modifié depuis son ouverture.
    
MAPI_E_OBJECT_DELETED 
  
> L'objet a été supprimé depuis son ouverture.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp:: SaveChanges** rend permanentes les modifications de propriété pour les objets qui prennent en charge le modèle de transaction de traitement, tels que les messages, les pièces jointes, les conteneurs de carnet d'adresses et les objets utilisateur de messagerie. Les objets qui ne prennent pas en charge les transactions, tels que les dossiers, les banques de messages et les sections de profil, rendent immédiatement les modifications permanentes. Aucun appel à **SaveChanges** n'est requis. 
  
Étant donné que les fournisseurs de services n'ont pas besoin de générer un identificateur d'entrée pour leurs objets tant que toutes les propriétés n'ont pas été enregistrées, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) d'un objet ne peut pas être disponible tant qu'elle n'a pas été exécutée en tant que méthode **SaveChanges** a été appelé. Certains fournisseurs attendent que l'indicateur KEEP_OPEN_READONLY soit défini sur l'appel de **SaveChanges** . KEEP_OPEN_READONLY indique que les modifications à enregistrer dans l'appel actif seront les dernières modifications apportées à l'objet. 
  
Certaines implémentations de la Banque de messages n'affichent pas les messages nouvellement créés dans un dossier jusqu'à ce qu'un client enregistre les modifications apportées aux messages à l'aide de **SaveChanges** et libère les objets message à l'aide de la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . De plus, certaines implémentations d'objets ne peuvent pas générer une propriété **PR_ENTRYID** pour un objet nouvellement créé tant que l'appel de **SaveChanges** n'a pas été effectué, et certains ne peuvent le faire qu'après l'appel de **SAVECHANGES** à l'aide de KEEP_OPEN_READONLY défini dans _ulFlags_.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous recevez l'indicateur KEEP_OPEN_READONLY, vous avez la possibilité de laisser l'accès de l'objet en lecture/écriture. Toutefois, un fournisseur ne peut jamais laisser un objet en lecture seule lorsque l'indicateur KEEP_OPEN_READWRITE est passé.
  
Lorsqu'un client enregistre plusieurs pièces jointes dans plusieurs messages, il appelle la méthode **SaveChanges** pour chaque pièce jointe et chaque message. Souvent, les clients définissent MAPI_DEFERRED_ERRORS pour chacun de ces appels, à l'exception de la dernière. Vous pouvez renvoyer des erreurs avec le dernier appel ou les appels précédents. Vous pouvez même ignorer l'indicateur. 
  
Si KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY est défini avec MAPI_DEFERRED_ERRORS, vous pouvez ignorer la demande d'erreur de défermentation. Si MAPI_DEFERRED_ERRORS n'est pas défini dans _ulFlags_, l'une des erreurs différées précédemment peut être renvoyée pour l'appel de **SaveChanges** . 
  
Si un fournisseur de transport distant fournit une implémentation fonctionnelle de cette méthode est facultatif et dépend d'autres choix de conception dans votre implémentation. Si vous implémentez cette méthode, faites-le en fonction de la documentation ici. Étant donné que les objets de dossier et les objets d'État ne sont pas traités, l'implémentation d' **SaveChanges** d'un fournisseur de transport distant au minimum doit retourner S_OK sans effectuer de travail. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si un client passe KEEP_OPEN_READONLY, appelle la méthode [IMAPIProp:: SetProps](imapiprop-setprops.md) , puis appelle de nouveau **SaveChanges** , la même implémentation peut échouer. 
  
Après avoir reçu MAPI_E_NO_ACCESS à partir d'un appel dans lequel vous avez défini KEEP_OPEN_READWRITE, vous continuerez à avoir accès en lecture/écriture à l'objet. Vous pouvez appeler de nouveau **SaveChanges** , en passant l'indicateur KEEP_OPEN_READONLY ou aucun indicateur avec KEEP_OPEN_SUFFIX. 
  
La prise en charge de l'indicateur KEEP_OPEN_READWRITE par un fournisseur dépend de l'implémentation du fournisseur. 
  
Pour indiquer que le seul appel à effectuer sur l'objet après **SaveChanges** est **IUnknown:: Release**, ne définissez aucun indicateur pour le paramètre _ulFlags_ . Une erreur de **SaveChanges** indique qu'il n'a pas pu faire en sorte que les modifications en attente soient permanentes. Les différents fournisseurs gèrent l'absence d'indicateurs différemment sur l'appel de **SaveChanges** . Certains fournisseurs traitent cet état de la même manière que KEEP_OPEN_READONLY; d'autres fournisseurs l'interprètent comme KEEP_OPEN_READWRITE. D'autres fournisseurs arrêtent l'objet lorsqu'ils ne reçoivent pas d'indicateurs sur l'appel de **SaveChanges** . 
  
Certaines propriétés, généralement des propriétés calculées, ne peuvent pas être traitées tant que vous n'avez pas appelé **SaveChanges** et, dans certains cas, **Release**.
  
Lorsque vous effectuez des modifications en bloc, telles que l'enregistrement de pièces jointes à plusieurs messages, différer le traitement des erreurs en définissant l'indicateur MAPI_DEFERRED_ERRORS dans _ulFlags_. Si vous enregistrez plusieurs pièces jointes dans plusieurs messages, **** effectuez un appel à chaque pièce jointe et un appel **SaveChanges** à chaque message. Définissez l'indicateur MAPI_DEFERRED_ERRORS pour chaque appel de pièce jointe et pour tous les messages à l'exception de la dernière. 
  
Si **SaveChanges** renvoie MAPI_E_OBJECT_CHANGED, vérifiez si l'objet d'origine a été modifié. Si c'est le cas, avertissez l'utilisateur, qui peut demander que les modifications remplacent les modifications précédentes ou enregistrer l'objet ailleurs. Si l'objet d'origine a été supprimé, avertissez-le de l'utilisateur pour lui permettre d'enregistrer l'objet à un autre emplacement. 
  
Vous ne pouvez pas appeler **SaveChanges** avec l'indicateur FORCE_SAVE sur un objet Open qui a été supprimé. 
  
Si **SaveChanges** renvoie une erreur, l'objet dont les modifications doivent être enregistrées reste ouvert, quels que soient les indicateurs définis dans le paramètre _ulFlags_ . 
  
> [!IMPORTANT]
> Les _ulFlags_ NON_EMS_XP_SAVE et SPAMFILTER_ONSAVE ne sont peut-être pas définis dans le fichier d'en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l'ajouter à votre code en utilisant les valeurs suivantes: >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Pour plus d'informations, consultez la rubrique [enregistrement des propriétés MAPI](saving-mapi-properties.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Enregistrement des propriétés MAPI](saving-mapi-properties.md)

