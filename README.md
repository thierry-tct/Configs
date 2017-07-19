# Configs


// Add parent's mutant set.  std::unordered_set<MutationIDType> parentsMutants;

// BBname of BB containing mutant (ex: if.cond).  std::string BBTypename;

// AST parent llvm::instruction type.   std::string astparentOpcodeName;  // = pInst->getOpcodeName.

std::unorded_set<MutantIDType> mutantsofbb;
for (auto &inst: *bb) {
  mutantsofbb.insert(ir2mutants.at(&inst).begin(), ir2mutants.at(&inst).end());
  
}
