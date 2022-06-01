---
title: DTBLBUTTON
description: DTBLBUTTON contient des informations sur un contrôle bouton pour une boîte de dialogue créée à partir d’une table d’affichage.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
ms.openlocfilehash: 45f823bfec7e2807f1c90056e3b1ef2be082ffb1
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816471"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient des informations sur un contrôle de bouton pour une boîte de dialogue créée à partir d’une table d’affichage.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro associée :  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
```cpp
typedef struct _DTBLBUTTON
{
  ULONG ulbLpszLabel;
  ULONG ulFlags;
  ULONG ulPRControl;
} DTBLBUTTON, FAR *LPDTBLBUTTON;

```

## <a name="members"></a>Members

 **ulbLpszLabel**
  
> Position en mémoire de la chaîne de caractères affichée sur le bouton.
    
 **ulFlags**
  
> Masque de bits des indicateurs utilisés pour désigner le format de l’étiquette pointée par le membre **ulbLpszLabel** . L’indicateur suivant peut être défini : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, l’étiquette est au format ANSI.
    
 **ulPRControl**
  
> Balise de propriété pour une propriété de type PT_OBJECT qui implémente l’interface [IMAPIControl](imapicontroliunknown.md) . Lorsque vous cliquez sur le bouton, MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour l’implémentation [IMAPIProp](imapipropiunknown.md) de la table d’affichage pour récupérer cette propriété. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLBUTTON** décrit un bouton d’un contrôle qui, lorsqu’il est cliqué, permet à un utilisateur de commencer une opération. En règle générale, le fait de cliquer sur un bouton entraîne l’affichage d’une boîte de dialogue modale ou l’appel d’une tâche par programmation. Les fournisseurs de services peuvent implémenter n’importe quoi via un contrôle de bouton. Si le bouton est censé effectuer une tâche basée sur les valeurs d’autres contrôles, ces contrôles doivent avoir défini l’indicateur DT_SET_IMMEDIATE. 
  
Le membre **ulbLpszLabel** est la position en mémoire de la chaîne de caractères affichée sur le bouton. Les fournisseurs de services peuvent ajouter un caractère ampersand (&amp;) pour indiquer un accélérateur Windows dans l’étiquette du bouton. Appuyer sur une touche d’accélérateur a le même effet que cliquer sur le bouton. 
  
Le membre **ulPRControl** décrit une propriété d’objet qui, lorsqu’elle est ouverte avec la méthode **IMAPIProp::OpenProperty** , retourne un pointeur vers un objet de contrôle. L’implémentation d’un objet de contrôle qui prend en charge l’interface **IMAPIControl** est un moyen d’étendre l’ensemble de fonctionnalités MAPI et de définir l’opération ou la tâche qui se produit lorsque vous cliquez sur le bouton. **IMAPIControl** fournit deux méthodes pour manipuler des boutons : [GetState](imapicontrol-getstate.md) pour désactiver ou activer les boutons et [Activer](imapicontrol-activate.md) pour gérer les clics de bouton. 
  
Pour obtenir une vue d’ensemble des tables d’affichage, consultez [Tables d’affichage](display-tables.md). Pour plus d’informations sur l’implémentation d’une table d’affichage, consultez [Implémentation d’une table d’affichage](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

