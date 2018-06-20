---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: d6a53d112e4c12cd9092ac627e99cf3c13d901f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784393"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**S’applique à**: Outlook 
  
Offre la possibilité de récupérer et de modifier l’accès pour les propriétés d’un objet. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Exposés par :  <br/> |Objet de données de propriété  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services et applications clientes  <br/> |
|Identificateur de l’interface :  <br/> |IID_IMAPIPropData  <br/> |
|Type de pointeur :  <br/> |LPPROPDATA  <br/> |
|Modèle de transaction :  <br/> |Nontransacted  <br/> |
   
## <a name="vtable-order"></a>Ordre vtable

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |D�finit le niveau d'acc�s de l'objet.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Définit le niveau d’accès et l’état d’un ou plusieurs des propriétés de l’objet.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |R�cup�re le niveau d'acc�s et l'�tat d'un ou plusieurs des propri�t�s de l'objet.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.  <br/> |
   
## <a name="remarks"></a>Remarques

L’interface **IPropData::IMAPIProp** est implémentée par MAPI et utilisé principalement par les fournisseurs de services qui accèdent à cette implémentation en appelant la fonction [CreateIProp](createiprop.md) . 
  
Pour plus d’informations sur les niveaux d’accès sur les objets et propriétés, voir [les autorisations pour les objets et propriétés](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

