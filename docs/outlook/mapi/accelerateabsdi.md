---
title: ACCELERATEABSDI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ACCELERATEABSDI
api_type:
- HeaderDef
ms.assetid: da67dcf4-1411-4fc9-992c-115485019bd3
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 46e87caa68a45a188272340db408c52546f02a57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322126"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Définit une fonction de rappel pour traiter les touches d'accès rapide dans une boîte de dialogue Carnet d'adresses non modal. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs. h  <br/> |
|Fonction définie implémentée par:  <br/> |MAPI  <br/> |
|Fonction définie appelée par:  <br/> |Applications clientes  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> dans Valeur propre à l'implémentation utilisée pour passer des informations d'interface utilisateur à une fonction. Dans les applications qui s'exécutent sur Microsoft Windows, _ulUIParam_ est le descripteur de fenêtre parente pour une boîte de dialogue et type HWND, casté en **ULONG_PTR**. La valeur zéro indique qu'il n'y a aucune fenêtre parent. 
    
 _lpvmsg_
  
> dans Pointeur vers un message Windows.
    
## <a name="return-value"></a>Valeur renvoyée

Une fonction avec le prototype **ACCELERATEABSDI** renvoie la valeur true si elle gère le message. 
  
## <a name="remarks"></a>Remarques

Une fonction basée sur le prototype **ACCELERATEABSDI** est utilisée uniquement avec une boîte de dialogue non modale, c'est-à-dire, uniquement si l'application cliente a défini l'indicateur DIALOG_SDI dans le membre _ulFlags_ de la structure [ADRPARM](adrparm.md) . 
  
Une boîte de dialogue non modale partage la boucle de messages Windows de l'application cliente, au lieu d'avoir sa propre boucle. L'application, qui contrôle la boucle de messages, ne sait pas quelles clés d'accélérateur la boîte de dialogue utilise, afin qu'elle appelle une fonction basée sur **ACCELERATEABSDI** pour tester et agir sur des clés d'accélérateur telles que Ctrl + P pour l'impression. 
  
La boucle de messages d'un client appelle la fonction basée sur **ACCELERATEABSDI** lorsque le client appelle une boîte de dialogue Carnet d'adresses sans mode avec la méthode [IAddrBook:: Address](iaddrbook-address.md) . Cet appel est terminé lorsque MAPI appelle une fonction basée sur le prototype de fonction [DISMISSMODELESS](dismissmodeless.md) . 
  

