---
title: À propos de l’inscription des magasins pour l’indexation
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a36c4dd63b2aea02cba03620642720967a5c9e8b
ms.sourcegitcommit: eb9453e5664b01759b602cb5a4cef5b4885128f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/24/2022
ms.locfileid: "63781193"
---
# <a name="about-registering-stores-for-indexing"></a>À propos de l’inscription des magasins pour l’indexation

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique est spécifique à la recherche instantanée dans Microsoft Office Outlook 2007.
  
La recherche instantanée vous permet de trouver rapidement des éléments dans Outlook. Il utilise des composants de Windows recherche de bureau.
  
Le handler de protocole MAPI vérifie la Windows registre pour les magasins qu’il doit indexer à des fins de recherche. Les fournisseurs du Windows Store qui souhaitent être indexés doivent être inscrits dans Windows registre.
  
Par défaut, Windows Recherche de bureau ajoute les quatre types de fournisseurs de magasins suivants au Registre Windows pour autoriser l’indexation :
  
- Store pour les fichiers de dossiers personnels (. PST).
    
-  Microsoft Exchange store, y compris les fichiers de dossier hors connexion (.ost). 
    
-  Stockez les dossiers publics. 
    
-  Store for Microsoft Office Outlook Connector for MSN. 
    
 Les fournisseurs de magasins tiers qui souhaitent être indexés doivent s’inscrire eux-mêmes dans Windows registre. 
  
> [!NOTE]
> Les administrateurs et les utilisateurs peuvent utiliser un paramètre de stratégie de groupe pour empêcher Windows recherche de bureau d’indexer Outlook éléments. Pour plus d’informations, voir [Extending Windows Desktop Search](https://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Clés de Registre

Sur un ordinateur, tous les fournisseurs de magasins qui souhaitent être indexés doivent être enregistrés sous l’une des trois clés de Registre suivantes dans le Windows registre. Le handler de protocole MAPI examine chacune de ces clés dans l’ordre suivant :
  
1. [HKLM]\Software\Policies\Microsoft\Windows\Windows Search\
    
2. [HKLM]\Software\Microsoft\Windows\Windows Search\Preferences\
    
3. [HKCU]\Software\Microsoft\Windows\Windows Search\Preferences\
    
 Chaque valeur sous la clé correspond à un fournisseur de magasins qui serait indexé. Le nom de la valeur est l’identificateur global unique (GUID) du fournisseur de magasins, qui est du type **DWORD** et a la valeur hexadécimale 0x00000001. 
  
## <a name="guids-for-store-providers"></a>GUID pour les fournisseurs du Store

La propriété MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** le GUID d’un magasin MAPI. Les GUID des fournisseurs de magasins qui Outlook index sont décrits dans le tableau suivant. 
  
|Type de fournisseur du Store |GUID |Notes |
|:-----|:-----|:-----|
|Fichiers dossiers personnels (. PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |Le GUID est documenté dans le fichier d’en-tête public mspst.h **comme MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |Le GUID est documenté dans le fichier d’en-tête public edkmdb.h en tant que **pbExchangeProviderPrimaryUserGuid** <br/> |
|Dossiers publics  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |Le GUID est documenté dans le fichier d’en-tête public edkmdb.h en tant que **pbExchangeProviderPublicGuid** <br/> |
|Outlook connector pour MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Aucune  <br/> |
   
## <a name="see-also"></a>Voir aussi



[À propos de l’API de magasin](about-the-store-api.md)

