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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6cf51985e534434c584eff4d63dfbf239121ee85
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436572"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Ajoute des dossiers de messages interpersonnels standard à une magasin de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Pointeur vers l’objet de magasin de messages auquel ajouter les dossiers. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour contrôler la façon dont les dossiers sont créés. Les indicateurs suivants peuvent être définies :
    
MAPI_FORCE_CREATE 
  
> Les dossiers doivent être vérifiés avant leur création, même si les propriétés de la boutique de messages indiquent qu’elles sont valides. Une application cliente définit généralement cet indicateur lorsqu’une erreur indique que la structure d’un dossier existant a été endommagée. 
    
MAPI_FULL_IPM_TREE 
  
> L’ensemble complet des dossiers IPM doit être créé dans le dossier racine de la boutique de messages. Les titres des dossiers dans la hiérarchie sont :
    
    - Affichages des dossiers
    
    - Affichages communs
    
    - Search Root\*
    
    - Sous-arbre IPM\*
    
    - Boîte de réception
    
    - Boîte d’envoi
    
    - Éléments supprimés\*
    
    - Éléments envoyés
    
    où les trois dossiers marqués sont le jeu minimal créé même si \* l’MAPI_FULL_IPM_TREE n’a pas été définie. Une application cliente définit généralement cet indicateur lorsque la magasin de messages dans laquelle les dossiers doivent être créés est la boutique par défaut.
    
 _lpcValues_
  
> [in, out] Pointeur vers le nombre de structures [SPropValue](spropvalue.md) dans le tableau renvoyé dans le _paramètre lppProps._ La valeur du  _paramètre lpcValues_ peut être zéro si  _lppProps_ est NULL. 
    
 _lppProps_
  
> [in, out] Pointeur vers un pointeur vers un tableau de structures **SPropValue** qui contient des valeurs de propriété pour la propriété **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) et pour les propriétés d’identificateur d’entrée de dossier appropriées. Si **HrValidateIPMSubtree** crée une boîte de réception dans la boutique de messages, le tableau **SPropValue** inclut un identificateur d’entrée de boîte de réception avec une balise de propriété spéciale codée comme  `PROP_TAG(PT_BINARY, PROP_ID_NULL)` . Le _paramètre lppProps_ peut être NULL, ce qui indique que l’implémentation d’appel ne nécessite pas le retour d’un tableau **SPropValue.** 
    
 _lppMapiError_
  
> [out] Pointeur vers un pointeur vers une structure [MAPIERROR](mapierror.md) qui contient les informations de version, de composant et de contexte d’une erreur. Le  _paramètre lppMAPIError_ a la valeur NULL si aucune structure **MAPIERROR** n’est renvoyée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

MAPI utilise la fonction **HrValidateIPMSubtree** en interne pour construire la sous-arbre IPM standard dans une magasin de messages lors de la première ouverture de la boutique, ou lorsqu’une boutique est rendue la boutique par défaut. Cette fonction peut également être utilisée par les applications clientes pour valider ou réparer des dossiers de messages standard. 
  
 **HrValidateIPMSubtree** crée toujours les dossiers Racine de recherche et Sous-arbre IPM dans le dossier racine de la boutique et le dossier Éléments supprimés dans le dossier sous-arbre IPM. Le dossier sous-arbre IPM est la racine de la hiérarchie IPM dans cette magasin de messages. Le dossier Racine de la recherche peut être utilisé comme racine d’une sous-arbre pour les dossiers de résultats de recherche. 
  
Les clients IPM doivent afficher l’affichage de leur dossier en commençant par le dossier racine de la sous-arbre IPM et en affichant les dossiers enfants sous celui-ci. Les informations du dossier racine d’une magasin de messages ne doivent pas apparaître dans l’interface utilisateur d’un client. Cette fonctionnalité signifie que si un client doit masquer des informations, elles peuvent être mises dans le répertoire racine de la sous-arbre IPM, où elles ne sont pas visibles par l’utilisateur. En revanche, les applications non-IPM qui nécessitent que les messages et les dossiers soient invisibles pour l’utilisateur, par exemple dans une magasin de messages basée sur un serveur, peuvent les placer en dehors de la hiérarchie IPM. 
  
 **HrValidateIPMSubtree** définit la propriété **PR_VALID_FOLDER_MASK** pour indiquer si chaque dossier IPM qu’il crée possède un identificateur d’entrée valide. Les propriétés d’identificateur d’entrée suivantes de la magasin de messages sont définies sur les identificateurs d’entrée des dossiers correspondants et renvoyées dans le paramètre _lppProps_ avec PR_VALID_FOLDER_MASK **:** 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Espace réservé à [PROP_TAG](prop_tag.md) boîte de réception IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI utilise la **méthode HrValidateIPMSubtree** pour ajouter des dossiers standard à une magasin de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

