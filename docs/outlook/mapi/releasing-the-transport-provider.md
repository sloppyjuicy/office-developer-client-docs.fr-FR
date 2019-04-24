---
title: Publication du fournisseur de transport
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e0f37485-55c9-40f0-bc8c-48f7297f9f50
description: 'Derni�re modification�: lundi 7 d�cembre 2015'
ms.openlocfilehash: 41d953db8e00ff52cd09a27e2f7550f9f1879321
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328384"
---
# <a name="releasing-the-transport-provider"></a>Publication du fournisseur de transport

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque MAPI ou le spouleur MAPI se termine à l'aide d'un objet de connexion de transport:
  
1. MAPI ou le spouleur MAPI appelle la méthode [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) du fournisseur de transport. 
    
2. Le fournisseur de transport annule l'objet d'État en appelant la méthode [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) . Le fait que le fournisseur de transport invalide ou non les objets de message envoyés ou reçus au moment de l'appel **TransportLogoff** dépend des indicateurs transmis à **TransportLogoff**.
    
3. Le fournisseur de transport appelle la méthode [IUnknown:: Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l'objet de prise en charge pour supprimer la ligne du fournisseur de transport de la table d'État et supprimer des tables internes les identificateurs uniques (UID) qui ont été définis avec l' [IMAPISupport:: Méthode SetProviderUID](imapisupport-setprovideruid.md) . Il décrémente le nombre d'objets d'ouverture de session connus actifs sur cet objet fournisseur. Si le nombre atteint zéro, MAPI appelle la méthode [IXPProvider:: Shutdown](ixpprovider-shutdown.md) et la **libération** sur l'objet fournisseur. S'il s'agissait du dernier objet fournisseur connu utilisant cette DLL lors de ce processus, MAPI appelle la fonction **FreeLibrary** sur la dll ultérieurement. La mémoire de l'objet de prise en charge MAPI est libérée et la méthode de **libération** d'objet de prise en charge est renvoyée. 
    
4. La méthode **TransportLogoff** renvoie S_OK. 
    
5. MAPI ou le spouleur MAPI appelle la **version** de l'objet de connexion du fournisseur de transport. La mémoire de l'objet est libérée. 
    
6. MAPI ou le spouleur MAPI appelle **FreeLibrary** sur la dll du fournisseur. 
    
Pour des méthodes de robustesse, les objets Logon et Provider doivent être en mesure de gérer eux-mêmes les appels de la **version** finale sans avoir préalablement appelé leurs méthodes **TransportLogoff** ou **Shutdown** . Si **Release** est appelé dans ce cas, les fournisseurs de transport doivent traiter les appels comme si **TransportLogoff** ou **Shutdown** avait été appelé avec un argument zéro suivi de **Release**.
  

