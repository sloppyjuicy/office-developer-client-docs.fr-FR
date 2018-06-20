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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 0a60b813a52779b28124ab6d69b493def35b14aa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783917"
---
# <a name="imapipropsavechanges"></a>IMAPIProp::SaveChanges

  
  
**S’applique à**: Outlook 
  
Rend permanentes toutes les modifications qui ont été apportées à un objet depuis la dernière opération d’enregistrement. 
  
```cpp
HRESULT SaveChanges(
  ULONG ulFlags
);
```

## <a name="parameters"></a>Param�tres

 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui contrôle ce qui se passe à l’objet lorsque la méthode **IMAPIProp::SaveChanges** est appelée. Les indicateurs suivants peuvent être définis : 
    
NON_EMS_XP_SAVE
  
> Indique que le message n’a pas été remis à partir d’un serveur Microsoft Exchange. Cet indicateur doit être utilisé conjointement avec la méthode [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) et traitement avant que le magasin de fichiers (PST) de dossiers personnels avertit une des règles de l’indicateur ITEMPROC_FORCE pour indiquer à une banque de dossiers personnels que le message est éligible pour client d’écoute que le message est arrivé. Cette règle traitement s’applique uniquement aux nouveaux messages créés avec [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) sur un serveur qui n’est pas un serveur Exchange, auquel cas le serveur Exchange est ont déjà traités règles dans le message. 
    
FORCE_SAVE 
  
> Modifications doivent être écrites à l’objet écraser les modifications précédentes qui ont été apportées à l’objet, et l’objet doit être fermé. Autorisation de lecture/écriture doit être définie pour l’opération aboutisse. L’indicateur FORCE_SAVE est utilisé lorsqu’un appel précédent à **SaveChanges** MAPI_E_OBJECT_CHANGED. 
    
KEEP_OPEN_READONLY 
  
> Les modifications doivent être validées et l’objet doit être maintenue ouverte pour être lue. Aucune modification supplémentaire ne sera. 
    
KEEP_OPEN_READWRITE 
  
> Les modifications doivent être validées et l’objet doit être conservée à ouvrir pour l’autorisation en lecture-écriture. Cet indicateur est généralement défini lors de la première ouverture de l’objet d’autorisation en lecture-écriture. Les modifications suivantes à l’objet sont autorisées. 
    
MAPI_DEFERRED_ERRORS 
  
> Permet de **SaveChanges** renvoyer avec succès, éventuellement avant que les modifications ont été entièrement validées. 
    
SPAMFILTER_ONSAVE
  
> Permet de courrier indésirable de filtrage d’un message est enregistré. Prise en charge de filtrage du courrier indésirable est disponible uniquement si le type d’adresse de messagerie de l’expéditeur est SMTP Simple Mail Transfer Protocol (), et le message est enregistré dans un magasin d’un fichier de dossiers personnels (PST).
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L’engagement des modifications a réussi.
    
MAPI_E_NO_ACCESS 
  
> L’objet ne peuvent pas conserver ouverte pour un accès en lecture seule **SaveChanges** si KEEP_OPEN_READONLY est set ou autorisation en lecture/écriture si KEEP_OPEN_READWRITE est défini. Aucune modification n’est validée. 
    
MAPI_E_OBJECT_CHANGED 
  
> L’objet a été modifié depuis son ouverture.
    
MAPI_E_OBJECT_DELETED 
  
> L’objet a été supprimé car il a été ouvert.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::SaveChanges** apporte les modifications de propriété définitive pour les objets qui prennent en charge le modèle de transaction de traitement, telles que les messages, les pièces jointes, les conteneurs de carnet d’adresses et les objets utilisateur de messagerie. Les objets qui ne prennent pas en charge les transactions, telles que les dossiers et banques de messages aux sections de profil apporter des modifications permanentes immédiatement. Aucun appel à **SaveChanges** n’est requis. 
  
Car les fournisseurs de services n’ont pas à générer un identificateur d’entrée pour leurs objets jusqu'à ce que toutes les propriétés ont été enregistrées, la propriété **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) d’un objet peuvent ne pas être disponible qu’après la méthode **SaveChanges** a été appelée. Certains fournisseurs attendre jusqu'à ce que l’indicateur KEEP_OPEN_READONLY est défini sur l’appel de **SaveChanges** . KEEP_OPEN_READONLY indique que les modifications soient enregistrées dans l’appel en cours est le dernier des modifications qui seront effectuées sur l’objet. 
  
Certaines implémentations de banque de messages ne pas afficher nouvellement créé les messages dans un dossier jusqu'à un client enregistre le message passe à l’aide de **SaveChanges** et libère les objets de message à l’aide de la méthode [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) . En outre, certaines implémentations de l’objet ne peut pas générer une propriété **PR_ENTRYID** d’un objet nouvellement créé jusqu'à après **SaveChanges** a été appelée et certaines peuvent le faire qu’après **SaveChanges** a été appelée à l’aide de KEEP_OPEN_READONLY définir dans _ulFlags_.
  
## <a name="notes-to-implementers"></a>Remarques destinées aux responsables de l’implémentation

Si vous recevez l’indicateur KEEP_OPEN_READONLY, vous avez la possibilité de laisser des accès de l’objet en lecture-écriture. Toutefois, un fournisseur ne peut jamais laisser un objet dans un état en lecture seule lorsque l’indicateur KEEP_OPEN_READWRITE est passé.
  
Lorsqu’un client enregistre plusieurs pièces jointes à plusieurs messages, il appelle la méthode **SaveChanges** pour chaque pièce jointe et chaque message. Souvent, les clients définira MAPI_DEFERRED_ERRORS pour chacun de ces appels, à l’exception de la dernière série. Vous pouvez retourner les erreurs avec le dernier appel ou appels antérieures. Vous pouvez même ignorer l’indicateur. 
  
Si KEEP_OPEN_READWRITE ou KEEP_OPEN_READONLY est défini avec MAPI_DEFERRED_ERRORS, vous pouvez ignorer la demande de report d’erreur. Si MAPI_DEFERRED_ERRORS n’est pas définie dans _ulFlags_, l’erreur précédemment différée peut être renvoyé pour l’appel de **SaveChanges** . 
  
Si un fournisseur de transport à distance fournit une implémentation de cette méthode fonctionnelle est facultative et dépend des autres options de conception dans votre implémentation. Si vous implémentez cette méthode, le faire conformément à la documentation ici. Étant donné que les objets folder et les objets d’état ne sont pas traitées, au minimum implémentation d’un fournisseur de transport à distance de **SaveChanges** doit retourner S_OK sans réellement utilisé. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Si un client transmet KEEP_OPEN_READONLY, appelle la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) , puis appelle de nouveau **SaveChanges** , l’implémentation peut échouer. 
  
Après avoir reçu MAPI_E_NO_ACCESS à partir d’un appel dans lequel vous définissez KEEP_OPEN_READWRITE, vous pourrez ont l’autorisation de lecture/écriture à l’objet. Vous pouvez appeler **SaveChanges** , en passant l’indicateur KEEP_OPEN_READONLY ou aucun indicateur avec KEEP_OPEN_SUFFIX. 
  
Si un fournisseur prend en charge l’indicateur KEEP_OPEN_READWRITE dépend de l’implémentation du fournisseur. 
  
Pour indiquer que l’appel uniquement au niveau de l’objet après **SaveChanges** est **IUnknown::Release**, ne définissez aucun indicateur pour le paramètre _ulFlags_ . Une erreur de **SaveChanges** indique qu’il ne pourrait pas conserver les modifications en attente. Différents fournisseurs gèrent l’absence d’indicateurs de l’appel de **SaveChanges** différemment. Certains fournisseurs de traitent cet état comme KEEP_OPEN_READONLY ; autres fournisseurs d’interprètent la même que KEEP_OPEN_READWRITE. Toujours autres fournisseurs d’arrêter l’objet lorsqu’ils ne reçoivent pas les indicateurs de l’appel de **SaveChanges** . 
  
Certaines propriétés, les propriétés calculées en général, ne peuvent pas être traitées jusqu'à ce que vous appeliez **SaveChanges** et, dans certains cas, la **version**.
  
Lorsque vous apportez des modifications en bloc, telles que l’enregistrement de pièces jointes à plusieurs messages, différer l’erreur de traitement en définissant l’indicateur MAPI_DEFERRED_ERRORS dans _ulFlags_. Si vous enregistrez plusieurs pièces jointes à plusieurs messages, émettre un **SaveChanges** appeler pour chaque pièce jointe et un **SaveChanges** appeler à chaque message. Définir l’indicateur MAPI_DEFERRED_ERRORS pour chaque appel de la pièce jointe et pour tous les messages à l’exception de la dernière série. 
  
Si **SaveChanges** renvoie MAPI_E_OBJECT_CHANGED, vérifiez si l’objet d’origine a été modifié. Dans ce cas, avertir l’utilisateur, qui peut demander que les modifications de remplacement les modifications précédentes ou enregistrement l’objet ailleurs. Si l’objet d’origine a été supprimé, avertir l’utilisateur de leur donner la possibilité d’enregistrer l’objet dans un autre emplacement. 
  
Vous ne pouvez pas appeler **SaveChanges** avec l’indicateur FORCE_SAVE sur un objet ouvert qui a été supprimé. 
  
Si **SaveChanges** renvoie une erreur, l’objet dont les modifications ont été le point d’être enregistrées reste ouvert, quel que soit les indicateurs définis dans le paramètre _ulFlags_ . 
  
> [!IMPORTANT]
> _ulFlags_ NON_EMS_XP_SAVE et SPAMFILTER_ONSAVE ne peuvent pas être définis dans le fichier d’en-tête téléchargeables que vous avez actuellement, auquel cas vous pouvez l’ajouter à votre code à l’aide des valeurs suivantes : >`#define SPAMFILTER_ONSAVE ((ULONG) 0x00000080)`>  `#define NON_EMS_XP_SAVE ((ULONG) 0x00001000)`
  
Pour plus d’informations, voir [L’enregistrement des propriétés MAPI](saving-mapi-properties.md).
  
## <a name="see-also"></a>Voir aussi



[IMAPIProp::SetProps](imapiprop-setprops.md)
  
[Propriété canonique PidTagEntryId](pidtagentryid-canonical-property.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[L’enregistrement des propriétés MAPI](saving-mapi-properties.md)

