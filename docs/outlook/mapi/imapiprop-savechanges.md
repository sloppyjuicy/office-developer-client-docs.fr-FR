---
title: IMAPIPropSaveChanges
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.SaveChanges
api_type:
- COM
ms.assetid: 864dbc3e-2039-435a-a279-385d79d1d13f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 1e20228e04440491ee5af5be3d79e2c6f4f5cdd7
ms.sourcegitcommit: 5969c693475e22a3f5a4fdde3473ecc33013b76f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/09/2022
ms.locfileid: "62462121"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Rend permanentes les modifications apportées à un objet depuis la dernière opération d’enregistrer. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle ce qu’il advient de l’objet lorsque la méthode **IMAPIProp::SaveChanges** est appelée. Les indicateurs suivants peuvent être définies : 
    
NON_EMS_XP_SAVE
  
> Indique que le message n’a pas été remis à partir d’un Microsoft Exchange Server. Cet indicateur doit être utilisé en combinaison avec la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) et l’indicateur ITEMPROC_FORCE pour indiquer à un magasin PST que le message est éligible pour le traitement des règles avant que le magasin de dossiers personnels (PST) informe tout client d’écoute que le message est arrivé. Ce traitement des règles s’applique uniquement aux nouveaux messages créés avec [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) sur un serveur qui n’est pas un Exchange Server, auquel cas le Exchange Server aurait déjà traitée des règles sur le message. 
    
FORCE_SAVE 
  
> Les modifications doivent être écrites dans l’objet, en remplacement des modifications précédentes apportées à l’objet, et l’objet doit être fermé. Une autorisation de lecture/écriture doit être définie pour que l’opération réussisse. L FORCE_SAVE est utilisé après un appel précédent à **SaveChanges** renvoyé MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> Les modifications doivent être déterminées et l’objet doit rester ouvert en lecture. Aucune modification supplémentaire n’est apportée. 
    
KEEP_OPEN_READWRITE 
  
> Les modifications doivent être déterminées et l’objet doit rester ouvert pour une autorisation de lecture/écriture. Cet indicateur est généralement définie lors de la première ouverture de l’objet pour une autorisation de lecture/écriture. Les modifications ultérieures apportées à l’objet sont autorisées. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet à **SaveChanges de** renvoyer correctement, éventuellement avant que les modifications n’ont été entièrement engagés. 
    
SPAMFILTER_ONSAVE
  
> Active le filtrage du courrier indésirable sur un message enregistré. La prise en charge du filtrage du courrier indésirable n’est disponible que si le type d’adresse e-mail de l’expéditeur suit le protocole SMTP et que le message est enregistré dans une banque pour un fichier de dossiers personnels (PST).
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> L’engagement de modifications a réussi.
    
MAPI_E_NO_ACCESS 
  
> **SaveChanges ne** peut pas conserver l’objet ouvert pour une autorisation en lecture seule si KEEP_OPEN_READONLY est définie, ou une autorisation de lecture/écriture si KEEP_OPEN_READWRITE est définie. Aucune modification n’est apportée. 
    
MAPI_E_OBJECT_CHANGED 
  
> L’objet a changé depuis son ouverture.
    
MAPI_E_OBJECT_DELETED 
  
> L’objet a été supprimé depuis son ouverture.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::SaveChanges** rend les modifications de propriété permanentes pour les objets qui prend en charge le modèle de traitement des transactions, tels que les messages, les pièces jointes, les conteneurs de carnet d’adresses et les objets utilisateur de messagerie. Les objets qui ne peuvent pas prendre en charge les transactions, tels que les dossiers, les magasins de messages et les sections de profil, modifient immédiatement de façon permanente. Aucun appel à **SaveChanges n’est** requis. 
  
Étant donné que les fournisseurs de services n’ont pas à générer d’identificateur d’entrée pour leurs objets tant que toutes les propriétés n’ont pas été enregistrées, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) d’un objet peut ne pas être disponible tant que sa méthode **SaveChanges** n’a pas été appelée. Certains fournisseurs attendent que l’indicateur KEEP_OPEN_READONLY est définie sur l’appel **SaveChanges** . KEEP_OPEN_READONLY indique que les modifications à enregistrées dans l’appel actuel seront les dernières modifications apportées à l’objet. 
  
Certaines implémentations de magasin de messages n’affiche pas les messages nouvellement créés dans un dossier tant qu’un client n’enregistre pas les modifications apportées aux messages à l’aide de **SaveChanges** et libère les objets de message à l’aide de la méthode [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) . En outre, certaines implémentations d’objets ne peuvent pas générer une propriété **PR_ENTRYID** pour un objet nouvellement créé tant que **SaveChanges** n’a pas été appelé, et d’autres ne peuvent le faire qu’après l’appel de **SaveChanges** à l’aide de KEEP_OPEN_READONLY définie dans  _ulFlags_.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Si vous recevez l’KEEP_OPEN_READONLY, vous avez la possibilité de laisser l’accès de l’objet en lecture/écriture. Toutefois, un fournisseur ne peut jamais laisser un objet en lecture seule lorsque l’KEEP_OPEN_READWRITE est passé.
  
Lorsqu’un client enregistre plusieurs pièces jointes dans plusieurs messages, il appelle la méthode **SaveChanges** pour chaque pièce jointe et chaque message. Souvent, les clients MAPI_DEFERRED_ERRORS pour chacun de ces appels, à l’exception du dernier. Vous pouvez renvoyer des erreurs avec le dernier appel ou les appels précédents. Vous pouvez même ignorer l’indicateur. 
  
Si une KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY est définie avec MAPI_DEFERRED_ERRORS, vous pouvez ignorer la demande de report d’erreur. Si MAPI_DEFERRED_ERRORS n’est pas définie dans  _ulFlags_, l’une des erreurs différées précédemment peut être renvoyée pour l’appel **SaveChanges** . 
  
Si un fournisseur de transport distant fournit une implémentation fonctionnelle de cette méthode est facultatif et dépend d’autres choix de conception dans votre implémentation. Si vous implémentez cette méthode, faites-le conformément à la documentation ici. Étant donné que les objets de dossier et les objets d’état ne sont pas transactionn s, au minimum l’implémentation **d’SaveChanges** par un fournisseur de transport distant doit renvoyer S_OK sans réellement faire de travail. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Si un client passe KEEP_OPEN_READONLY, appelle la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) , puis appelle **à nouveau SaveChanges** , la même implémentation peut échouer. 
  
Après avoir reçu MAPI_E_NO_ACCESS d’un appel dans lequel vous avez KEEP_OPEN_READWRITE, vous continuerez à avoir une autorisation de lecture/écriture sur l’objet. Vous pouvez appeler **à nouveau SaveChanges** , en passant l’KEEP_OPEN_READONLY ou aucun indicateur avec KEEP_OPEN_SUFFIX. 
  
Le fait qu’un fournisseur prend en charge KEEP_OPEN_READWRITE’indicateur dépend de l’implémentation du fournisseur. 
  
Pour indiquer que le seul appel à appeler sur l’objet après **SaveChanges** est **IUnknown::Release**, ne définissez aucun indicateur pour le  _paramètre ulFlags_ . Une erreur **de SaveChanges indique** qu’il n’a pas pu rendre permanentes les modifications en attente. Différents fournisseurs gèrent différemment l’absence d’indicateurs sur **l’appel SaveChanges** . Certains fournisseurs traitent cet état de la même façon que KEEP_OPEN_READONLY ; d’autres fournisseurs l’interprètent de la même KEEP_OPEN_READWRITE. D’autres fournisseurs arrêtent l’objet lorsqu’ils ne reçoivent pas d’indicateurs lors de l’appel **SaveChanges** . 
  
Certaines propriétés, généralement calculées, ne peuvent pas être traitées tant que vous n’avez pas appelé **SaveChanges** et, dans certains cas, **Release**.
  
Lorsque vous a majeurez des modifications, telles que l’enregistrement de pièces jointes dans plusieurs messages, reportez le traitement des erreurs en MAPI_DEFERRED_ERRORS’indicateur dans  _ulFlags_. Si vous enregistrez plusieurs pièces jointes dans plusieurs messages, faites un appel **SaveChanges** à chaque pièce jointe et un appel **SaveChanges** à chaque message. Définissez l MAPI_DEFERRED_ERRORS pour chaque appel de pièce jointe et pour tous les messages à l’exception du dernier. 
  
Si **SaveChanges renvoie** MAPI_E_OBJECT_CHANGED, vérifiez si l’objet d’origine a été modifié. Si c’est le cas, avertissez l’utilisateur, qui peut demander que les modifications ont changé ou enregistrer l’objet ailleurs. Si l’objet d’origine a été supprimé, avertissez l’utilisateur de lui donner la possibilité d’enregistrer l’objet à un autre emplacement. 
  
Vous ne pouvez pas **appeler SaveChanges** avec l’FORCE_SAVE sur un objet ouvert qui a été supprimé. 
  
Si **SaveChanges renvoie** une erreur, l’objet dont les modifications doivent être enregistrées reste ouvert, quels que soient les indicateurs définies dans le _paramètre ulFlags_ . 
  
> [!IMPORTANT]
> Les NON_EMS_XP_SAVE  _ulFlags_ et SPAMFILTER_ONSAVE peuvent ne pas être définis dans le fichier d’en-tête téléchargeable dont vous disposez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide des valeurs suivantes : >  `#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Pour plus d’informations, voir [Enregistrement des propriétés MAPI](saving-mapi-properties.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[Enregistrement des propriétés MAPI](saving-mapi-properties.md)

