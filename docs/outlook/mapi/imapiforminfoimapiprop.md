---
title: IMAPIFormInfo IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo
api_type:
- COM
ms.assetid: a9fda518-11ba-42aa-85ef-dd2279e0319d
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2b2abf4440ee2d81a8e95dcdb5fde2daeaa6e6f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575909"
---
# <a name="imapiforminfo--imapiprop"></a>IMAPIFormInfo : IMAPIProp

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Fournit l’accès client applications aux propriétés qui sont spécifiques à la définition du formulaire. En conservant les informations d’un formulaire dans un objet séparé, le fournisseur de bibliothèque formulaire permet de décrire un formulaire à un client sans activer le formulaire.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |MAPIForm.h  <br/> |
|Exposés par :  <br/> |Objets d’informations de formulaire  <br/> |
|Implémentée par :  <br/> |Fournisseurs de bibliothèques de formulaires  <br/> |
|Appelée par :  <br/> |Applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIFormInfo  <br/> |
|Type de pointeur :  <br/> |LPMAPIFORMINFO  <br/> |
|Modèle de transaction :  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[CalcFormPropSet](imapiforminfo-calcformpropset.md) <br/> |Retourne un pointeur vers l’ensemble complet des propriétés qui utilise un formulaire.  <br/> |
|[CalcVerbSet](imapiforminfo-calcverbset.md) <br/> |Retourne un pointeur vers l’ensemble complet des verbes qui utilise un formulaire.  <br/> |
|[MakeIconFromBinary](imapiforminfo-makeiconfrombinary.md) <br/> |Crée une icône à partir d’une propriété de l’icône d’un formulaire.  <br/> |
|[SaveForm](imapiforminfo-saveform.md) <br/> |Enregistre une description d’un formulaire particulier dans un fichier de configuration.  <br/> |
|[OpenFormContainer](imapiforminfo-openformcontainer.md) <br/> |Retourne un pointeur vers le conteneur de formulaire dans lequel un formulaire particulier est installé.  <br/> |
   
## <a name="remarks"></a>Remarques

Contrairement à la plupart des interfaces définies dans le fichier d’en-tête MapiForm.h, **IMAPIFormInfo** hérite de l’interface [IMAPIProp](imapipropiunknown.md) , car il exporte la plupart des informations d’un formulaire via des appels à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

