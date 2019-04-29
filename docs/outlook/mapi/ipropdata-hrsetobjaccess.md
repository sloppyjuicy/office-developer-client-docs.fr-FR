---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425154"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
D�finit le niveau d'acc�s de l'objet.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Paramètres

 _ulAccess_
  
> [in] Un masque de bits d'indicateurs qui sp�cifie le niveau d'acc�s de l'objet. Vous pouvez d�finir un des indicateurs suivants :
    
IPROP_READONLY 
  
> D�finit le niveau d'acc�s de l'objet en lecture seule. 
    
IPROP_READWRITE 
  
> D�finit le niveau d'acc�s de l'objet en lecture/�criture.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Niveau d'acc�s de l'objet a �t� correctement d�fini.
    
## <a name="remarks"></a>Remarques

La m�thode **IPropData::HrSetObjAccess** d�finit le niveau d'acc�s pour un objet dans son int�gralit�, et non des propri�t�s individuelles. **HrSetObjAccess** peut �tre utilis� pour modifier le niveau d'acc�s �tabli lorsque l'objet a �t� cr��. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour d�finir un niveau d'acc�s sur une propri�t�, d'abord appeler **HrSetObjAccess** avec l'indicateur IPROP_READWRITE dans le param�tre  _ulAccess_ pour rendre l'objet modifiable. Puis appelez la m�thode [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , en sp�cifiant la propri�t� cible dans le tableau indiqu� par le param�tre  _lpPropTagArray_. 
  
Pour cr�er un objet avec des propri�t�s qui seront en lecture seule aux clients, cr�ez un objet en lecture-�criture, ajoutez les propri�t�s n�cessaires et ensuite appeler **HrSetObjAccess** pour modifier l'acc�s de l'objet en lecture seule. 
  
Vous pouvez �galement utiliser **HrSetObjAccess** pour emp�cher les clients de cr�er de nouvelles propri�t�s. 
  
## <a name="see-also"></a>Voir aussi



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

