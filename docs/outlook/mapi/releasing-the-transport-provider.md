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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386221"
---
# <a name="releasing-the-transport-provider"></a>Publication du fournisseur de transport

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque MAPI ou le spouleur MAPI est terminée à l’aide d’un objet de connexion de transport :
  
1. MAPI ou le spouleur MAPI appelle la méthode de [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) du fournisseur de transport. 
    
2. Le fournisseur de transport invalide l’objet d’état en appelant la méthode [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) . Si le fournisseur de transport invalide les objets de message sont envoyées ou reçues au moment de l’appel **TransportLogoff** varie selon les indicateurs qui ont été transmis à **TransportLogoff**.
    
3. Le fournisseur de transport appelle la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de la prise en charge pour supprimer la ligne du fournisseur de transport à partir de la table d’état et de supprimer des tables internes des identificateurs uniques (UID) qui ont été définies avec la [IMAPISupport :: SetProviderUID](imapisupport-setprovideruid.md) méthode. Il décrémente le nombre d’objets connus d’ouverture de session actives sur cet objet fournisseur. Si le nombre est égal à zéro, MAPI appelle la méthode [IXPProvider::Shutdown](ixpprovider-shutdown.md) et la **version** de l’objet fournisseur. S’il s’agissait du dernier objet connus fournisseur à l’aide de cette DLL sur ce processus, MAPI appelle la fonction **FreeLibrary** sur la DLL à une date ultérieure. La mémoire pour l’objet de prise en charge MAPI est libérée et renvoie l’objet de prise en charge de méthode de **publication** . 
    
4. La méthode **TransportLogoff** renvoie S_OK. 
    
5. MAPI ou le spouleur MAPI appelle **Release** sur un objet de connexion du fournisseur de transport. La mémoire pour l’objet est publiée. 
    
6. MAPI ou le spouleur MAPI appelle **FreeLibrary** sur la DLL du fournisseur. 
    
Pour robustesse, les objets d’ouverture de session et le fournisseur doivent être en mesure de gérer les appels **version** finales sur eux-mêmes sans avoir leur **TransportLogoff** ou les méthodes de **l’arrêt de** l’appelé. Si la **version** est appelée dans ce cas, les fournisseurs de transport doivent traiter les appels comme **TransportLogoff** ou **l’arrêt** avait été appelée avec un zéro argument, suivi de **version**.
  

