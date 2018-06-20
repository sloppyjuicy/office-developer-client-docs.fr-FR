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
ms.openlocfilehash: b7d4d758f7031c55aa3a23b662ec8727ea1e0719
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782870"
---
# <a name="accelerateabsdi"></a>ACCELERATEABSDI
 
**S’applique à**: Outlook 
  
Définit une fonction de rappel de processus raccourcis dans une boîte de dialogue non modale adresse téléchargeable. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapidefs.h  <br/> |
|Fonction implémentée par :  <br/> |MAPI  <br/> |
|Fonction appelée par :  <br/> |Applications clientes  <br/> |
   
```cpp
BOOL (STDMETHODCALLTYPE ACCELERATEABSDI)( 
  ULONG_PTR ulUIParam,
  LPVOID lpvmsg
);
```

## <a name="parameters"></a>Paramètres

 _ulUIParam_
  
> [in] Une valeur spécifique à l’implémentation utilisée pour transmettre des informations d’interface utilisateur à une fonction. Dans les applications s’exécutant sur Microsoft Windows, _ulUIParam_ est le handle de fenêtre parent pour une boîte de dialogue et de type HWND, d’une **ULONG_PTR entière**. La valeur zéro indique aucune fenêtre parent est. 
    
 _lpvmsg_
  
> [in] Pointeur vers un message Windows.
    
## <a name="return-value"></a>Valeur renvoy�e

Une fonction avec le prototype **ACCELERATEABSDI** renvoie la valeur TRUE si elle gère le message. 
  
## <a name="remarks"></a>Remarques

Une fonction basée sur le prototype **ACCELERATEABSDI** est utilisée uniquement avec une boîte de dialogue non modale, c'est-à-dire, uniquement si l’application cliente a défini l’indicateur DIALOG_SDI dans le membre _ulFlags_ de la structure [ADRPARM](adrparm.md) . 
  
Une boîte de dialogue non modale partage boucle de message de l’application cliente Windows, au lieu d’avoir sa propre boucle. L’application, qui contrôle la boucle de messages, ne sait pas les touches accélérateur les utilisations de boîte de dialogue, elle appelle une **ACCELERATEABSDI** fondé sur fonction pour tester et modifier les touches accélérateur par exemple CTRL + P pour l’impression. 
  
Appels de boucle de message d’un client l' **ACCELERATEABSDI** en fonction de fonction lorsque le client appelle une boîte de dialogue non modale adresse livre avec la méthode [IAddrBook::Address](iaddrbook-address.md) . Cet appel est terminé lorsque MAPI appelle une fonction basée sur le prototype de fonction [DISMISSMODELESS](dismissmodeless.md) . 
  

