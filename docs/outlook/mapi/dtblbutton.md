---
title: DTBLBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.DTBLBUTTON
api_type:
- COM
ms.assetid: 6058c78b-05d4-45a3-988c-1fbf8322125e
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e0797364eb4ec24793f64bad2f4d838507c236e4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571065"
---
# <a name="dtblbutton"></a>DTBLBUTTON

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Contient des informations sur un contrôle bouton pour une boîte de dialogue établi à partir d’un tableau d’affichage.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Macro connexe :  <br/> |[SizedDtblButton](sizeddtblbutton.md) <br/> |
   
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
  
> Position dans la mémoire de la chaîne de caractères qui s’affiche sur le bouton.
    
 **ulFlags**
  
> Masque de bits d’indicateurs utilisés pour désigner le format de l’étiquette vers laquelle pointé le membre **ulbLpszLabel** . Vous pouvez définir l’indicateur suivant : 
    
MAPI_UNICODE 
  
> L’étiquette est au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas définie, l’étiquette est au format ANSI.
    
 **ulPRControl**
  
> Balise de propriété pour une propriété de type PT_OBJECT qui implémente l’interface [IMAPIControl](imapicontroliunknown.md) . Lorsque le bouton est activé, MAPI appelle la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) pour la mise en œuvre de la table affichage [IMAPIProp](imapipropiunknown.md) d’extraire cette propriété. 
    
## <a name="remarks"></a>Remarques

Une structure **DTBLBUTTON** décrit un contrôle bouton qui, lorsque vous cliquez dessus, permet à un utilisateur commencer une opération. En règle générale, un bouton entraîne une boîte de dialogue modale s’affiche ou des tâches de programmation à appeler. Fournisseurs de service peuvent implémenter rien via un contrôle bouton. Si le bouton est supposé effectuer une tâche en fonction des valeurs d’autres contrôles, ces contrôles doivent avoir défini l’indicateur DT_SET_IMMEDIATE. 
  
Le membre **ulbLpszLabel** est la position dans la mémoire de la chaîne de caractères qui s’affiche sur le bouton. Fournisseurs de services peuvent ajouter une esperluette (&amp;) pour indiquer un raccourci Windows dans l’étiquette du bouton. Appuyer sur une touche d’accès rapide a le même effet qu’un clic sur le bouton. 
  
Le membre **ulPRControl** décrit une propriété d’objet qui, lorsque ouvert avec la méthode **IMAPIProp::OpenProperty** , retourne un pointeur vers un objet control. Implémentation d’un objet de contrôle qui prend en charge l’interface **IMAPIControl** consiste à étendre le jeu de fonctions MAPI et définir l’opération ou la tâche qui se produit lorsque l’utilisateur clique sur le bouton. **IMAPIControl** fournit deux méthodes pour la manipulation des boutons : [GetState](imapicontrol-getstate.md) pour désactiver ou activer les boutons et [Activer](imapicontrol-activate.md) pour gérer les clics de bouton. 
  
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). Pour plus d’informations sur la façon d’implémenter un tableau d’affichage, consultez [l’implémentation d’une Table à afficher](display-table-implementation.md).
  
## <a name="see-also"></a>Voir aussi



[DTCTL](dtctl.md)


[Structures MAPI](mapi-structures.md)

