---
title: Libération du fournisseur de transport
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
# <a name="releasing-the-transport-provider"></a>Libération du fournisseur de transport

 
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lorsque MAPI ou lepooler MAPI a terminé d’utiliser un objet de transport :
  
1. MAPI ou lepooler MAPI appelle la méthode [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) du fournisseur de transport. 
    
2. Le fournisseur de transport invalide l’objet d’état en appelant la méthode [IMAPISupport::MakeInvalid.](imapisupport-makeinvalid.md) Si le fournisseur de transport invalide les objets de message qui sont envoyés ou reçus au moment de l’appel **TransportLogoff** dépend des indicateurs qui ont été transmis à **TransportLogoff**.
    
3. Le fournisseur de transport appelle la méthode [IUnknown::Release](https://msdn.microsoft.com/library/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a%28Office.15%29.aspx) de l’objet de support pour supprimer la ligne du fournisseur de transport de la table d’état et supprimer des tables internes les identificateurs uniques (UID) qui ont été définies avec la méthode [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md) Il décrémente le nombre d’objets d’accès connus actifs sur cet objet fournisseur. Si le nombre atteint zéro, MAPI appelle la méthode [IXPProvider::Shutdown](ixpprovider-shutdown.md) et **Release** sur l’objet fournisseur. S’il s’agit du dernier objet fournisseur connu utilisant cette DLL sur ce processus, MAPI appelle ultérieurement la fonction **FreeLibrary** sur la DLL. La mémoire de l’objet de prise en charge MAPI est libérée et la méthode **Release** de l’objet de support renvoie. 
    
4. La **méthode TransportLogoff** renvoie S_OK. 
    
5. MAPI ou lepooler MAPI appelle **Release** sur l’objet d’accès au fournisseur de transport. La mémoire de l’objet est libérée. 
    
6. MAPI ou lepooler MAPI appelle **FreeLibrary** sur la DLL du fournisseur. 
    
Pour des raisons de robustesse, les objets  d’ouverture de ligne et de fournisseur doivent être en mesure de gérer eux-mêmes les appels de version finale sans avoir d’abord appelé leurs méthodes **TransportLogoff** ou **Shutdown.** Si **Release** est appelé dans ce cas, les fournisseurs de transport doivent traiter les appels comme si **TransportLogoff** ou **Shutdown** avait été appelé avec un argument zéro suivi de **Release**.
  

