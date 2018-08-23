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
ms.openlocfilehash: d7886d08c21e8fff9aceb3437ecb6bbbd970ed7b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591421"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
D�finit le niveau d'acc�s de l'objet.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Param�tres

 _ulAccess_
  
> [in] Un masque de bits d'indicateurs qui sp�cifie le niveau d'acc�s de l'objet. Vous pouvez d�finir un des indicateurs suivants :
    
IPROP_READONLY 
  
> D�finit le niveau d'acc�s de l'objet en lecture seule. 
    
IPROP_READWRITE 
  
> D�finit le niveau d'acc�s de l'objet en lecture/�criture.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Niveau d'acc�s de l'objet a �t� correctement d�fini.
    
## <a name="remarks"></a>Remarques

La m�thode **IPropData::HrSetObjAccess** d�finit le niveau d'acc�s pour un objet dans son int�gralit�, et non des propri�t�s individuelles. **HrSetObjAccess** peut �tre utilis� pour modifier le niveau d'acc�s �tabli lorsque l'objet a �t� cr��. 
  
## <a name="notes-to-callers"></a>Notes aux appelants

Pour d�finir un niveau d'acc�s sur une propri�t�, d'abord appeler **HrSetObjAccess** avec l'indicateur IPROP_READWRITE dans le param�tre  _ulAccess_ pour rendre l'objet modifiable. Puis appelez la m�thode [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , en sp�cifiant la propri�t� cible dans le tableau indiqu� par le param�tre  _lpPropTagArray_. 
  
Pour cr�er un objet avec des propri�t�s qui seront en lecture seule aux clients, cr�ez un objet en lecture-�criture, ajoutez les propri�t�s n�cessaires et ensuite appeler **HrSetObjAccess** pour modifier l'acc�s de l'objet en lecture seule. 
  
Vous pouvez �galement utiliser **HrSetObjAccess** pour emp�cher les clients de cr�er de nouvelles propri�t�s. 
  
## <a name="see-also"></a>Voir aussi



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

