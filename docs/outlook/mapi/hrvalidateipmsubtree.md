---
title: HrValidateIPMSubtree
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrValidateIPMSubtree
api_type:
- COM
ms.assetid: 6454c1fa-5216-4934-a908-48c634ac4a07
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346766"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute des dossiers de message interpersonnels standard à une banque de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
   
```cpp
HrValidateIPMSubtree(
  LPMDB lpMDB,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppProps,
  LPMAPIERROR FAR * lppMapiError
);
```

## <a name="parameters"></a>Paramètres

 _lpMDB_
  
> dans Pointeur vers l'objet de la Banque de messages à laquelle les dossiers doivent être ajoutés. 
    
 _ulFlags_
  
> dans Masque de des indicateurs utilisés pour contrôler la façon dont les dossiers sont créés. Les indicateurs suivants peuvent être définis:
    
MAPI_FORCE_CREATE 
  
> Les dossiers doivent être vérifiés avant la création, même si les propriétés de la Banque de messages indiquent qu'elles sont valides. Une application cliente définit généralement cet indicateur lorsqu'une erreur indique que la structure d'un dossier existant a été endommagée. 
    
MAPI_FULL_IPM_TREE 
  
> L'ensemble complet des dossiers IPM doit être créé dans le dossier racine de la Banque de messages. Les titres de dossier dans la hiérarchie sont les suivants:
    
    - Vues de dossier
    
    - Affichages courants
    
    - Racine de recherche\*
    
    - Sous-arborescence IPM\*
    
    - Boîte de réception
    
    - Boîte d'envoi
    
    - Éléments supprimés\*
    
    - Éléments envoyés
    
    où les trois dossiers marqués \* sont le jeu minimum créé, même lorsque l'indicateur MAPI_FULL_IPM_TREE n'a pas été défini. Une application cliente définit généralement cet indicateur lorsque la Banque de messages dans laquelle les dossiers doivent être créés est la Banque par défaut.
    
 _lpcValues_
  
> [in, out] Pointeur vers le nombre de structures [SPropValue](spropvalue.md) dans le tableau renvoyé dans le paramètre _lppProps_ . La valeur du paramètre _lpcValues_ peut être zéro si _lppProps_ est null. 
    
 _lppProps_
  
> [in, out] Pointeur vers un pointeur vers un tableau de structures **SPropValue** qui contient des valeurs de propriété pour la propriété **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) et pour les propriétés d'identificateur d'entrée de dossier appropriées. Si **HrValidateIPMSubtree** crée une boîte de réception dans la Banque de messages, le tableau **SPropValue** inclut un identificateur d'entrée de boîte de réception avec `PROP_TAG(PT_BINARY, PROP_ID_NULL)`une balise de propriété spéciale codée en tant que. Le paramètre _lppProps_ peut être null, ce qui indique que l'implémentation de l'appel ne nécessite pas le renvoi d'un tableau **SPropValue** . 
    
 _lppMapiError_
  
> remarquer Pointeur vers un pointeur vers une structure [MAPIERROR](mapierror.md) qui contient les informations de version, de composant et de contexte pour une erreur. Le paramètre _lppMAPIError_ est défini sur null si aucune structure **MAPIERROR** n'est renvoyée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

MAPI utilise la fonction **HrValidateIPMSubtree** en interne pour construire la sous-arborescence IPM standard dans une banque de messages lors de la première ouverture de la banque ou lorsqu'une banque devient la Banque par défaut. Cette fonction peut également être utilisée par les applications clientes pour valider ou réparer des dossiers de messages standard. 
  
 **HrValidateIPMSubtree** crée toujours les dossiers racine de recherche et sous-arborescence IPM dans le dossier racine de la Banque et le dossier éléments supprimés dans le dossier sous-arborescence IPM. Le dossier de sous-arborescence IPM est la racine de la hiérarchie IPM dans ce magasin de messages. Le dossier racine de recherche peut être utilisé comme racine d'une sous-arborescence pour les dossiers de résultats de recherche. 
  
Les clients IPM doivent afficher l'affichage de leur dossier en commençant par le dossier racine de la sous-arborescence IPM et en affichant les dossiers enfants en dessous. Les informations contenues dans le dossier racine d'une banque de messages ne doivent pas apparaître dans l'interface utilisateur d'un client. Cette fonctionnalité signifie que si un client doit masquer les informations, les informations peuvent être placées dans le répertoire racine de la sous-arborescence IPM, où il n'est pas visible par l'utilisateur. En revanche, les applications non-IPM qui nécessitent que des messages et des dossiers soient invisibles pour l'utilisateur, par exemple dans une banque de messages basée sur un serveur, peuvent les placer en dehors de la hiérarchie IPM. 
  
 **HrValidateIPMSubtree** définit la propriété **PR_VALID_FOLDER_MASK** pour indiquer si chaque dossier IPM créé a un identificateur d'entrée valide. Les propriétés d'identificateur d'entrée suivantes de la Banque de messages sont définies sur les identificateurs d'entrée des dossiers correspondants et renvoyés dans le paramètre _lppProps_ avec **PR_VALID_FOLDER_MASK**: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Un espace réservé [PROP_TAG](prop_tag.md) pour la boîte de réception IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MstStoreDlg. cpp  <br/> |CMsgStoreDlg:: OnValidateIPMSubtree  <br/> |MFCMAPI utilise la méthode **HrValidateIPMSubtree** pour ajouter des dossiers standard à une banque de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

