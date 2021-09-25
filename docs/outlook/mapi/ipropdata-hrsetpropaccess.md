---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 13e90fdd80c6a41963dd0f3081739038b190abe5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596021"
---
# <a name="ipropdatahrsetpropaccess"></a>IPropData::HrSetPropAccess

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
D�finit le niveau d'acc�s ou un �tat pour un ou plusieurs des propri�t�s de l'objet.
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propri�t�s qui indiquent les propri�t�s � modifier. 
    
 _rgulAccess_
  
> [in] Tableau des masques de bits indicateur. Chaque masque de bits indique les niveaux d'acc�s ou �tat ou les deux, pour chacune des propri�t�s identifi�es dans le tableau vers laquelle pointe le param�tre  _lpPropTagArray_. Les deux tableaux sont positionnels dans la mesure o� le premier masque de bits dans  _rgulAccess_ d�crit la premi�re propri�t� qui pointe  _lpPropTagArray_, et ainsi de suite. Pour chaque balise de propri�t�, un indicateur de niveau d'acc�s et l'indicateur d'�tat d'un seul peut �tre d�finie. Le tableau suivant pr�sente les indicateurs possibles. 
    
|**Indicateur de niveau d'acc�s**|**Indicateur d'�tat**|
|:-----|:-----|
|IPROP_READONLY, ce qui indique que la propri�t� ne peut pas �tre modifi�e.  <br/> |IPROP_CLEAN, ce qui indique que la propri�t� n'a pas �t� modifi�e.  <br/> |
|IPROP_READWRITE, ce qui indique que la propri�t� peut �tre modifi�e.  <br/> |IPROP_DIRTY, ce qui indique que la propri�t� a �t� modifi�e.  <br/> |
   
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les indicateurs d'�tat et le niveau d'acc�s ont �t� correctement d�finis.
    
MAPI_E_NO_ACCESS 
  
> Une tentative a �t� effectu�e pour d�finir la propri�t� sur un objet en lecture seule ou d'un objet pour lequel l'appelant dispose d'autorisations insuffisantes.
    
MAPI_E_INVALID_PARAMETER 
  
> Le param�tre  _rgulAccess_ contient une combinaison d'indicateurs, tels que IPROP_READONLY et IPROP_READWRITE non valide. 
    
## <a name="remarks"></a>Remarques

La m�thode **IPropData::HrSetPropAccess** modifie le niveau d'acc�s et l'�tat pour les propri�t�s qui sont identifi�es par les balises de propri�t� dans la structure [SPropTagArray](sproptagarray.md) d�sign�s par le param�tre  _lpPropTagArray_. Pour chaque propri�t�, il existe une entr�e correspondante dans le tableau  _rgulAccess_. L'entr�e peut �tre d�finie sur un indicateur qui indique le niveau d'acc�s de la propri�t� et l'autre indicateur indiquant son statut. 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Utilisez **HrSetPropAccess** pour d�terminer quand une valeur de propri�t� particuli�re change et modifier le niveau d'acc�s pour un ou plusieurs des propri�t�s d'un objet. 
  
## <a name="see-also"></a>Voir aussi



[SPropTagArray](sproptagarray.md)
  
[IPropData : IMAPIProp](ipropdataimapiprop.md)

