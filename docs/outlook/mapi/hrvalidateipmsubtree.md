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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2625b148d15c2f5ccf65eedf3a1b1f2c9d0d133e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592044"
---
# <a name="hrvalidateipmsubtree"></a>HrValidateIPMSubtree

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Ajoute les dossiers de messages interpersonnels standard (IPM) à une banque de messages. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
   
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

 _IpMDB_
  
> [in] Pointeur vers le message stocker d’objet à laquelle ajouter les dossiers. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs utilisés pour contrôler la façon dont les dossiers sont créés. Les indicateurs suivants peuvent être définis :
    
MAPI_FORCE_CREATE 
  
> Les dossiers doivent être vérifiées avant la création, même si les propriétés de banque de messages indiquent qu’ils sont valides. En règle générale, une application cliente définit cet indicateur lorsqu’une erreur indique que la structure d’un dossier existant a été endommagée. 
    
MAPI_FULL_IPM_TREE 
  
> L’ensemble des dossiers IPM doit être créé dans le dossier racine de la banque messages. Les titres de dossier dans la hiérarchie sont les suivants :
    
    - Vues de dossiers
    
    - Affichages communs
    
    - Racine de la recherche\*
    
    - Sous-arborescence IPM\*
    
    - Inbox
    
    - La boîte d’envoi
    
    - Éléments supprimés\*
    
    - Éléments envoyés
    
    où les trois dossiers marquée avec \* sont l’ensemble minimal créé même si l’indicateur MAPI_FULL_IPM_TREE n’a pas été définie. En règle générale, une application cliente définit cet indicateur lors de la banque de messages dans lequel les dossiers sont créées est la banque par défaut.
    
 _lpcValues_
  
> [entrée, sortie] Pointeur vers le nombre de structures [SPropValue](spropvalue.md) dans le tableau renvoyé dans le paramètre _lppProps_ . La valeur du paramètre _lpcValues_ peut être zéro si _lppProps_ est NULL. 
    
 _lppProps_
  
> [entrée, sortie] Pointeur vers un pointeur vers un tableau de structures **SPropValue** qui contient les valeurs de propriété pour la propriété **PR_VALID_FOLDER_MASK** ([PidTagValidFolderMask](pidtagvalidfoldermask-canonical-property.md)) et pour les propriétés d’identificateur de l’entrée dossier approprié. Si **HrValidateIPMSubtree** crée une boîte de réception dans la banque de messages, le tableau **SPropValue** inclut un identificateur d’entrée de boîte de réception avec une balise de propriété spéciale codée en tant que `PROP_TAG(PT_BINARY, PROP_ID_NULL)`. Le paramètre _lppProps_ peut être de valeur NULL, indiquant que la mise en œuvre appelant ne nécessite pas renvoyer d’une matrice **SPropValue** . 
    
 _lppMapiError_
  
> [out] Pointeur vers un pointeur vers une structure [MAPIERROR](mapierror.md) qui contient des informations de version, composant et le contexte d’une erreur. Le paramètre _lppMAPIError_ est défini sur la valeur NULL si aucune structure **MAPIERROR** n’est renvoyée. 
    
## <a name="return-value"></a>Valeur renvoyée

Aucun.
  
## <a name="remarks"></a>Remarques

MAPI utilise la fonction **HrValidateIPMSubtree** en interne pour construire la sous-arborescence IPM standard dans une banque de messages lors de la première ouverture de la banque, ou lorsqu’une banque est apportée à la valeur par défaut stocker. Cette fonction peut également être utilisée par les applications clientes pour valider ou réparer des dossiers de messages standard. 
  
 **HrValidateIPMSubtree** crée toujours les dossiers racine de la recherche et la sous-arborescence IPM dans le dossier du magasin racine et le dossier éléments supprimés dans le dossier de la sous-arborescence IPM. Le dossier de la sous-arborescence IPM est la racine de la hiérarchie de l’IPM de cette banque de messages. Le dossier racine de la recherche peut servir de la racine d’une sous-arborescence pour les dossiers de résultats de recherche. 
  
Clients IPM doivent afficher leur mode dossier Démarrage dans le dossier racine de la sous-arborescence IPM et affichera enfants ses sous-dossiers. Pour plus d’informations dans le dossier racine d’une banque de messages n’apparaissent pas dans l’interface utilisateur d’un client. Cette fonctionnalité signifie que si un client doit masquer les informations, les informations peuvent être placées dans le répertoire racine de la sous-arborescence IPM, où il n’est pas visible à l’utilisateur. En revanche, les applications non-IPM nécessitant des messages et des dossiers à être invisibles pour l’utilisateur, par exemple dans une banque de messages sur le serveur, les placerez en dehors de la hiérarchie IPM. 
  
 **HrValidateIPMSubtree** définit la propriété **PR_VALID_FOLDER_MASK** pour indiquer si chaque dossier IPM crée possède un identificateur d’entrée valide. Les propriétés d’identificateur de l’entrée suivantes de la banque de messages sont définies sur les identificateurs d’entrée des dossiers correspondants et retournées dans le paramètre _lppProps_ avec **PR_VALID_FOLDER_MASK**: 
  
 **PR_COMMON_VIEWS_ENTRYID** ([PidTagCommonViewsEntryId](pidtagcommonviewsentryid-canonical-property.md))
  
> **PR_FINDER_ENTRYID** ([PidTagFinderEntryId](pidtagfinderentryid-canonical-property.md))
  
> **PR_IPM_OUTBOX_ENTRYID** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
  
> **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
  
> **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
  
> **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
  
> **PR_VIEWS_ENTRYID** ([PidTagViewsEntryId](pidtagviewsentryid-canonical-property.md))
  
> Un espace réservé [PROP_TAG](prop_tag.md) pour la boîte de réception IPM (PT_BINARY, PROP_ID_NULL). 
    
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MstStoreDlg.cpp  <br/> |CMsgStoreDlg::OnValidateIPMSubtree  <br/> |MFCMAPI utilise la méthode **HrValidateIPMSubtree** pour ajouter des dossiers standards à une banque de messages.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)

