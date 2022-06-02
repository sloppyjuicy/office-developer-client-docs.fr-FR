---
title: IPropDataHrGetPropAccess
description: IPropData HrGetPropAccess récupère le niveau d’accès et l’état d’une ou plusieurs des propriétés de l’objet.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
ms.openlocfilehash: a722168a6b8ef171deb9f3eab612286024e08694
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65826896"
---
# <a name="ipropdatahrgetpropaccess"></a>IPropData::HrGetPropAccess

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
R�cup�re le niveau d'acc�s et l'�tat d'un ou plusieurs des propri�t�s de l'objet.
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a>Paramètres

 _lppPropTagArray_
  
> [entr�e, sortie] � l'entr�e, un tableau de balises de propri�t�s qui indiquent les propri�t�s pour lequel r�cup�rer des niveaux d'acc�s et l'�tat ; dans le cas contraire, un pointeur null, ce qui indique que **HrGetPropAccess** doit extraire les niveaux d'acc�s et l'�tat de toutes les propri�t�s. Dans la sortie, un tableau de balises de propri�t� pour les indicateurs d'acc�s et l'�tat ont �t� r�cup�r�s. Les indicateurs sont stock�s dans le tableau indiqu� par le param�tre  _lprgulAccess_. 
    
 _lprgulAccess_
  
> [out] Pointeur vers un tableau de masques de bits indicateur. Chaque masque de bits indique les niveaux d'acc�s ou l'�tat ou les deux, pour chacune des propri�t�s identifi�es dans le tableau indiqu� par le param�tre  _lpPropTagArray_. Les deux tableaux sont positionnels dans la mesure o� le premier masque de bits que points  _lprgulAccess_ � d�crit la premi�re propri�t� que  _lpPropTagArray_ pointe, et ainsi de suite. Pour chaque balise de propri�t�, les indicateurs suivants peuvent �tre d�finis : 
    
|**Indicateur de niveau d'acc�s**|**Indicateur d'�tat**|
|:-----|:-----|
|IPROP_READONLY, ce qui indique que la propri�t� ne peut pas �tre modifi�e. |IPROP_CLEAN, ce qui indique que la propri�t� n'a pas �t� modifi�e. |
|IPROP_READWRITE, ce qui indique que la propri�t� peut �tre modifi�e. |IPROP_DIRTY, ce qui indique que la propri�t� a �t� modifi�e. |
   
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les indicateurs de niveau et l'�tat de l'acc�s pour les propri�t�s ont �t� renvoy�es avec succ�s.
    
## <a name="remarks"></a>Remarques

La m�thode **IPropData::HrGetPropAccess** r�cup�re un ensemble d'indicateurs qui indique le niveau d'acc�s et l'�tat d'une ou plusieurs propri�t�s. 
  
## <a name="notes-to-callers"></a>Remarques aux appelants :

Vous pouvez utiliser **HrGetPropAccess** dans les cas suivants : 
  
- Pour d�terminer si un client modifi� ou supprim� une propri�t� accessible en �criture.
    
- Pour emp�cher un client � partir de la modification ou suppression d'une propri�t� en utilisant les m�thodes [IMAPIProp](imapipropiunknown.md) . 
    
Si une des propri�t�s dans le tableau de balise de propri�t� d�sign�s par  _lppPropTagArray_ a �t� supprim�e, **HrGetPropAccess** d�finit l'entr�e du tableau � 0 � la sortie. Si vous d�finissez  _lppPropTagArray_ sur NULL et une des propri�t�s de l'objet a �t� supprim�e, la propri�t� deleted est renvoy�e dans le tableau. 
  
Si une propri�t� a �t� modifi�e, son indicateur IPROP_DIRTY est d�fini dans l'entr�e correspondante dans le tableau qui pointe  _lprgulAccess_. Ni IPROP_READONLY ni IPROP_READWRITE sera d�finie. 
  
Si une propri�t� n'a pas �t� modifi�e ou supprim�e, seul l'indicateur IPROP_READONLY ou IPROP_READWRITE sera d�finie. 
  
## <a name="see-also"></a>Voir aussi



[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

