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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435144"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Permet de récupérer et de modifier l’accès aux propriétés d’un objet. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Exposé par :  <br/> |Objet de données de propriété  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services et applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIPropData  <br/> |
|Type de pointeur :  <br/> |LPPROPDATA  <br/> |
|Modèle de transaction :  <br/> |Non traduit  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |D�finit le niveau d'acc�s de l'objet.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Définit le niveau d’accès et l’état d’une ou de plusieurs propriétés de l’objet.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |R�cup�re le niveau d'acc�s et l'�tat d'un ou plusieurs des propri�t�s de l'objet.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Ajoute une ou plusieurs propriétés de type PT_OBJECT à l’objet.  <br/> |
   
## <a name="remarks"></a>Remarques

**L’interface IPropData::IMAPIProp** est implémentée par MAPI et utilisée principalement par les fournisseurs de services qui accèdent à cette implémentation en appelant la fonction [CreateIProp.](createiprop.md) 
  
Pour plus d’informations sur les niveaux d’accès sur les objets et les propriétés, voir [Permissions for Objects and Properties](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Voir aussi



[Interfaces MAPI](mapi-interfaces.md)

