fs = import('fs')

infiles = [
  'ShieldBoostersECU.js.in',
  'EQ_ECU_SHIELDBOOSTERS_LICENCE.js.in',
  'ForwardWeaponECU.js.in',
  'EQ_ECU_FORWARDWEAPON_LICENCE.js.in',
  'EQ_ECU_FORWARDWEAPON.conditions.js.in',
  'EQ_WEAPON_ECU.conditions.js.in',
]

foreach infile : infiles
  if infile.endswith('.in')
    outfile = fs.stem(infile)
  else
    outfile = fs.name(infile)
  endif
  oxp_file = configure_file(
    input         : infile,
    output        : outfile,
    configuration : oxp_cfg_data,
  )
  oxp_files += oxp_file
endforeach
