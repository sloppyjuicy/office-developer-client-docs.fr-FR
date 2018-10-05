---
title: Définir par programme l’ordre de résolution des listes d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f9559afb-8db1-ce72-3e11-9b3d47bb80b6
description: 'Dernière modification : 06 juillet 2012'
ms.openlocfilehash: 4ca3e9d11a3133236d38ef31b01ecded932e8013
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392916"
---
# <a name="programmatically-set-the-resolution-order-for-address-lists"></a>Définir par programme l’ordre de résolution des listes d’adresses
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette rubrique contient un exemple de code en langage C++ qui définit par programmation l’ordre des listes d’adresses par les destinataires de courrier électronique messages et les participants dans les demandes de réunion sont résolus.
  
MAPI, chaque profil peut prendre en charge plusieurs listes d’adresses et chaque liste d’adresses réside dans son propre conteneur. MAPI prend en charge la méthode **[SetSearchPath](https://support.microsoft.com/kb/292590)** dans l’interface qui vous permet de définir un nouveau chemin d’accès de la recherche dans le profil qui est utilisé pour la résolution de nom. Pour utiliser la méthode **IAddrBook::SetSearchPath** , que vous aurez définir l’ordre de résolution de votre choix dans un tableau de **[SRowSet](srowset.md)** qui contient les conteneurs des carnets d’adresses pertinents dans l’ordre souhaité, puis spécifiez le tableau comme le *lpSearchPath*  paramètre. La première propriété de chaque entrée dans le tableau **SRowSet** doit être la propriété **[PR_ENTRYID](pidtagentryid-canonical-property.md)** du carnet d’adresses correspondant. 
  
L’exemple de code définit l’ordre de résolution dans les étapes suivantes :
  
1. Initialise `numANR` et le nombre de conteneurs en correspondance et spécifie les noms et l’ordre de résolution des listes d’adresses de votre choix dans une `ANROrder` tableau. 
    
2. Initialise MAPI à l’aide de la fonction **exécuter MAPIInitialize** . 
    
3.  Ouvre une session sur MAPI et permet à l’utilisateur à choisir un profil. 
    
4.  Obtient un pointeur vers le carnet d’adresses à partir de la session en cours. 
    
5. Ouvre le carnet d’adresses.
    
6. Ouvre le conteneur de la racine du carnet d’adresses.
    
7. Ouvre la table de hiérarchie du conteneur de carnet d’adresses racine.
    
8. Obtient la liste d’adresses conteneurs du carnet de dans la hiérarchie.
    
9. Recherche les ID d’entrée des listes d’adresses de votre choix en comparant les noms des listes d’adresses de votre choix dans `ANROrder` pour les noms dans la hiérarchie de carnets d’adresses existants. 
    
10. Définit l’identificateur d’entrée appropriée dans le tableau **SRowSet** , `pNewRows`.
    
11. Appelle et transmet `pNewRows` en tant que paramètre *lpSearchPath* pour **IAddrBook::SetSearchPath** pour définir le chemin de recherche. 
    
12. Nettoie les pointeurs et les mémoires tampons internes.
    
13. Ferme la session de MAPI.
    
14. Uninitalizes MAPI.
    
Cet exemple de code utilise des listes d’adresses qui sont disponibles dans l’installation par défaut de Microsoft Office Outlook : **Tous les Contacts**, **Tous les groupes**et les **Contacts**. Vous devez exécuter l’exemple après que Outlook est démarré et est en cours d’exécution sur un profil initialisé. L’exemple fonctionne correctement avec les noms qui se trouvent dans une seule langue (par exemple, tous les noms sont en anglais). Il n’est pas conçu pour fonctionner dans les déploiements multilingues, par exemple le dossier **Contacts** localisé pour un utilisateur qui exécutent une version anglaise Outlook. 
  
```cpp
#include "stdafx.h" 
#include <mapix.h> 
#include <mapiguid.h> 
#include <mapiutil.h> 
#include <mapidefs.h> 
#include <stdio.h> 
#include <conio.h> 
 
//Number of address lists to resolve against 
const int numANR = 3; 
WCHAR *ANROrder[numANR] = {_T("All Contacts"), _T("All Groups"), _T("Contacts")}; 
UINT  numContainersFound [numANR] = {0}; 
 
// Temporary structure to allocate buffer in MAPI. This will be used as a parent buffer to free space later. 
LPVOID tempLink; 
 
// Forward declaration of helper function to copy binary data 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent); 
 
void main() 
{ 
    // MAPI address book and session variables 
    HRESULT       hRes = S_OK;            // Result code returned from MAPI calls. 
    LPMAPISESSION lpSession = NULL;   // Pointer to MAPI session. 
    LPADRBOOK     lpAddrBook = NULL;  // Pointer to Address Book. 
 
    // Counters 
    ULONG         i = 0;                  // Index counter 
    ULONG         j = 0;                  // Index counter 
 
    // Used for querying hierarchy 
    ULONG                                   ulObjType = 0L;      // Object type returned by MAPI 
    LPMAPICONTAINER     pIABRoot = NULL;     // Root address book container 
    LPMAPITABLE              pHTable = NULL;      // Holds hierarchy table 
    LPSRowSet        pRows = NULL;        // Pointer to row set. Stores AB Address Lists 
 
    // Used for setting search path 
    LPSRowSet     pNewRows = NULL;        // Pointer to new row set 
    SizedSRowSet  (numANR, NewRows);      // New row set 
    SPropValue    sProps[numANR] = {0};   // Property tag structure 
 
    // Structures contaning MAPI Column Sets required for querying tables 
    enum { 
        abPR_ENTRYID, 
        abPR_DISPLAY_NAME_W, 
        abNUM_COLS}; 
 
    static SizedSPropTagArray(abNUM_COLS,abCols) = { 
        abNUM_COLS, 
        PR_ENTRYID, 
        PR_DISPLAY_NAME_W, 
    }; 
 
    // Initialize MAPI 
    if (FAILED ( hRes = MAPIInitialize(NULL))) goto Exit; 
 
    // Log on to MAPI and allow user to choose profile 
 
    // Note: This uses the current MAPI session if there is one 
    if (FAILED ( hRes = MAPILogonEx(NULL, NULL, NULL, MAPI_LOGON_UI, &lpSession))) goto Exit; 
 
    // Open the Address Book 
    if (FAILED (hRes = lpSession->OpenAddressBook(NULL, NULL, NULL, &lpAddrBook))) goto Cleanup; 
 
    // Open the Address Book Root container 
    if (FAILED (hRes = lpAddrBook -> OpenEntry ( 
        0L,  
        NULL, 
        NULL,  
        0L, 
        &ulObjType, 
        (LPUNKNOWN *) &pIABRoot ))) 
    goto Cleanup; 
 
    // Intentionally allocate 0 bytes. This is used for buffer management. 
    MAPIAllocateBuffer(0L, &tempLink);  
 
    // Make sure there is a Container object 
    // Query hierarchy for containers 
    if ( MAPI_ABCONT == ulObjType ) { 
        // - Call IMAPIContainer::GetHierarchyTable to open the Hierarchy 
        //   table of the root address book container 
        if ( FAILED ( hRes = pIABRoot -> GetHierarchyTable ( CONVENIENT_DEPTH | MAPI_UNICODE, 
            &pHTable ) ) ) 
        goto Cleanup; 
 
        // Get the list of address book containers first 
        if ( FAILED ( hRes = HrQueryAllRows (  
            pHTable, 
            (LPSPropTagArray) &abCols, 
            NULL, 
            NULL, 
            0L, 
            &pRows ) ) ) 
        goto Cleanup; 
 
        // Initialize the structures to set the search order 
        ZeroMemory(&NewRows, numANR * sizeof(SRow)); 
        pNewRows = (LPSRowSet)&NewRows; 
 
        // Set the number of rows you are going to set 
        pNewRows->cRows = numANR; 
 
        // Set the pointers to the structures 
        for (i=0; i<numANR; i++) 
            pNewRows->aRow[i].lpProps = &sProps[i]; 
 
        // Compare the list to the ones that of interest 
        for (i=0; i<pRows->cRows; i++) { 
            if (pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].ulPropTag == PR_DISPLAY_NAME_W) { 
                LPWSTR containerName =  pRows->aRow[i].lpProps[abPR_DISPLAY_NAME_W].Value.lpszW; 
                for (j=0; j<numANR; j++) 
                    if (!wcscmp (containerName, ANROrder[j])) { 
                        // First check if a container with this name has been found already 
                        if (numContainersFound[j] == 0) { 
                            numContainersFound[j]++; 
                            pNewRows->aRow[j].cValues = 1; 
 
                            // The property being passing is PR_ENTRY_ID 
                            pNewRows->aRow[j].lpProps[0].ulPropTag = PR_ENTRYID; 
 
                            // Copy the binary data over 
                            if (FAILED (hRes = CopySBinary( 
                                &pNewRows->aRow[j].lpProps[0].Value.bin, 
                                &pRows->aRow[i].lpProps[abPR_ENTRYID].Value.bin, 
                                tempLink))) {  
                                    printf ("Fatal Error:Failed to copy entry IDs\n"); 
                                    goto Cleanup; 
                            } 
                         } 
                         // More than 1 container matched the same name 
                         else {  
                             printf ("Fatal Error: Duplicate container found, container name = %s\n", containerName); 
                             goto Cleanup; 
                         } 
                    } 
            } 
        } 
 
        // Only set the search path if all the rows have been found 
        // Check the array for any entries that were blank 
        for (i=0; i< numANR; i++) 
            if (numContainersFound [i] == 0) { 
                printf ("Fatal Error: all containers were not found\n"); 
                goto Cleanup; 
            } 
 
        // Everything is safe to set the search path now 
        if (FAILED (hRes = lpAddrBook->SetSearchPath(0, pNewRows))) {                    
            printf ("Fatal Error: failed to set the search path\n"); 
            goto Cleanup; 
        } 
    } 
 
    Cleanup: 
        MAPIFreeBuffer(tempLink); 
        UlRelease(pHTable); 
        FreeProws(pRows); 
        UlRelease (pIABRoot); 
        UlRelease(lpAddrBook); 
 
        // Log off from MAPI 
        hRes = lpSession->Logoff(NULL, NULL, 0); 
        UlRelease(lpSession); 
 
    Exit: 
        // Uninitialize MAPI 
        MAPIUninitialize(); 
} 
 
///////////////////////////////////////////////////////////// 
//    CopySBinary() 
// 
//    Parameters 
// 
//    Purpose 
//      Allocates a new SBinary and copies psbSrc into it 
// 
 
STDMETHODIMP CopySBinary( 
    LPSBinary psbDest, 
    const LPSBinary psbSrc, 
    LPVOID pParent) 
{ 
    HRESULT     hRes = S_OK; 
    psbDest->cb = psbSrc->cb; 
 
    if (psbSrc->cb) { 
        if (pParent) 
            hRes = MAPIAllocateMore( 
                 psbSrc->cb, 
                 pParent, 
                 (LPVOID*) &psbDest->lpb); 
        else 
            hRes = MAPIAllocateBuffer( 
                 psbSrc->cb, 
                 (LPVOID*) &psbDest->lpb); 
 
    if (!FAILED(hRes)) 
        CopyMemory(psbDest->lpb,psbSrc->lpb,psbSrc->cb); 
    } 
 
   return hRes; 
} 

```

## <a name="see-also"></a>Voir aussi

- [À propos de la définition de l’ordre de résolution pour les listes d’adresses dans Outlook](about-setting-the-resolution-order-for-address-lists-in-outlook.md)

