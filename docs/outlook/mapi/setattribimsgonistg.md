---
title: SetAttribIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SetAttribIMsgOnIStg
api_type:
- COM
ms.assetid: 683d0d00-1b93-445d-86ff-180a3e6d2323
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: e8a0daa2afe2397f39b7f37a31ef718ba65a3350
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787136"
---
# <a name="setattribimsgonistg"></a>SetAttribIMsgOnIStg

  
  
**S’applique à**: Outlook 
  
Définit ou modifie les attributs de propriétés sur un objet [IMessage](imessageimapiprop.md) fournie par la fonction [OpenIMsgOnIStg](openimsgonistg.md) . 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |IMessage.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de magasin d’applications clientes et message  <br/> |
   
```cpp
HRESULT SetAttribIMsgOnIStg(
  LPVOID lpObject,
  LPSPropTagArray lpPropTags,
  LPSPropAttrArray lpPropAttrs,
  LPSPropProblemArray FAR * lppPropProblems
);
```

## <a name="parameters"></a>Paramètres

 _lpObject_
  
> [in] Pointeur vers l’objet pour la propriété attributs sont définies. 
    
 _lpPropTags_
  
> [in] Pointeur vers une structure [SPropTagArray](sproptagarray.md) contenant un tableau de balises de propriété indiquant les propriétés pour la propriété attributs sont définies. 
    
 _lpPropAttrs_
  
> [in] Pointeur vers une structure [SPropAttrArray](spropattrarray.md) répertoriant les attributs de propriété à définir. 
    
 _lppPropProblems_
  
> [out] Pointeur vers la structure [SPropProblemArray](spropproblemarray.md) retournée contenant un ensemble de problèmes de propriété. Cette structure identifie les problèmes rencontrés si **SetAttribIMsgOnIStg** a été en mesure de définir certaines propriétés, mais pas toutes. Si un pointeur null est passé dans le paramètre _lppPropProblems_ , aucun tableau de problème de propriété n’est renvoyé même si certaines propriétés n’ont pas été définies. 
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi, mais une ou plusieurs propriétés ne sont pas accessible et ont été renvoyées avec un type de propriété de PT_ERROR.
    
## <a name="remarks"></a>Remarques

Attributs de la propriété est accessible uniquement sur propriété objets, autrement dit, l’implémentation de la [IMAPIProp : IUnknown](imapipropiunknown.md) interface. Pour rendre les propriétés MAPI disponible sur un objet de stockage structuré OLE, [OpenIMsgOnIStg](openimsgonistg.md) génère une [IMessage : IMAPIProp](imessageimapiprop.md) objet en haut de l’objet OLE **IStorage** . Les attributs de propriété sur de tels objets peuvent définir ou a été modifiés avec **SetAttribIMsgOnIStg** et récupérés par [GetAttribIMsgOnIStg](getattribimsgonistg.md). 
  
 **Remarque** **GetAttribIMsgOnIStg** et **SetAttribIMsgOnIStg** ne fonctionnent pas sur tous les objets **IMessage** . Ils ne sont valides pour **IMessage**- sur - objets **IStorage** renvoyés par **OpenIMsgOnIStg**. 
  
Dans le paramètre _lpPropAttrs_ , le nombre et la position des attributs doivent correspondre le nombre et la position des balises de propriété passées dans le paramètre _lpPropTags_ . 
  
La fonction **SetAttribIMsgOnIStg** est utilisée pour définir les propriétés de message en lecture seule lorsque le schéma **IMessage** . L’exemple de fournisseur de magasin de message utilise à cet effet. Pour plus d’informations, voir [les Messages](mapi-messages.md). 
  

